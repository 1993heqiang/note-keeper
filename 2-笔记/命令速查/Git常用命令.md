## 命令

### config

- 查看配置项及来源

  ```shell
  # 查看所有配置及来源
  git config --show-origin --list

  # 查看特定配置项的来源
  git config --show-origin user.name

  # 查看匹配特定模式的配置项来源
  git config --show-origin --get-regexp user
  ```

- 为当前仓库配置访问令牌

  ```bash
  git config credential.helper store
  git config credential.username "你的GitCode用户名"
  # 首次拉代码时，密码输入刚才生成的PAT，Git会自动保存
  git pull
  ```

- ## 配置参数

### core.autocrlf

```shell
# 提交时会自动将CRLF转换为LF,检出时会将LF转换为CRLF,适用于Windows系统.
git config --global core.autocrlf true

# 提交时会自动将CRLF转换为LF,检出时不转换,适用于macOS和Linux.
git config --global core.autocrlf input

# 仅在Windows上开发时,关闭该特性可以将CRLF都保留在版本库中.
git config --global core.autocrlf false
```

---

## 多代码仓多账号数据隔离

### 核心思路

**主代码仓 = 全局默认身份**，不需要任何额外配置。其他代码托管平台统一放在 `~/workspace/multi-hub/` 下，通过 Git 的 `includeIf` 机制按目录自动切换身份、邮箱和代理。

### 第一步：确认全局配置（主代码仓身份）

全局 `~/.gitconfig` 保持不动，作为主代码仓（如 GitHub）的默认身份：

```ini
# ~/.gitconfig
[user]
    name = <your-main-username>
    email = <your-main-email@example.com>

[http]
    proxy = http://127.0.0.1:<your-proxy-port>
[https]
    proxy = http://127.0.0.1:<your-proxy-port>
```

### 第二步：创建多平台管理目录

```bash
mkdir -p ~/workspace/multi-hub/<platform-a>
# 例如：
# mkdir -p ~/workspace/multi-hub/gitcode
# mkdir -p ~/workspace/multi-hub/gitee
```

### 第三步：为每个平台创建独立配置文件

每个平台一个文件，命名规则 `~/.gitconfig-<platform>`：

**`~/.gitconfig-<platform-a>`**

```ini
[user]
    name = <platform-a-username>
    email = <platform-a-email@example.com>
```

如果某平台需要覆盖全局代理（比如不需要代理，或者需要不同的代理）：

```ini
# 不需要代理时，置空覆盖全局
[http]
    proxy =
[https]
    proxy =

# 或者使用不同的代理
[http]
    proxy = <another-proxy>
[https]
    proxy = <another-proxy>
```

### 第四步：在全局 `~/.gitconfig` 末尾追加 includeIf

**每个平台一条**，路径精确匹配到对应目录：

```ini
# ~/.gitconfig 末尾追加
[includeIf "gitdir:~/workspace/multi-hub/<platform-a>/"]
    path = ~/.gitconfig-<platform-a>

[includeIf "gitdir:~/workspace/multi-hub/<platform-b>/"]
    path = ~/.gitconfig-<platform-b>
```

> **规则**：一个平台 = 一个目录 + 一个配置文件 + 一条 `includeIf`，互不干扰。

### 第五步（可选）：主代码仓配置 SSH 免密登录

```bash
# 1. 生成专用密钥（推荐 ed25519）
ssh-keygen -t ed25519 -C "<your-main-email@example.com>" -f ~/.ssh/id_ed25519_<platform>

# 2. 将公钥添加到代码托管平台
cat ~/.ssh/id_ed25519_<platform>.pub
# GitHub: https://github.com/settings/keys
# GitLab: https://gitlab.com/-/profile/keys
# Gitee:  https://gitee.com/profile/sshkeys

# 3. 配置 ~/.ssh/config
```

`~/.ssh/config`：

```
Host <platform-host>       # 例如 github.com
    HostName <platform-host>
    User git
    IdentityFile ~/.ssh/id_ed25519_<platform>
    IdentitiesOnly yes
```

之后该平台仓库使用 SSH 地址克隆：`git clone git@<platform-host>:user/repo.git`

> 现有 HTTPS 地址的仓库也可切换：`git remote set-url origin git@<platform-host>:user/repo.git`

### 验证方法

```bash
# 主代码仓 — 应输出全局默认身份
cd ~/workspace/<any-repo-not-in-multi-hub>
git config user.name    # → <your-main-username>
git config user.email   # → <your-main-email@example.com>

# 其他平台 — 应输出对应平台身份
cd ~/workspace/multi-hub/<platform-a>/<any-repo>
git config user.name    # → <platform-a-username>
git config user.email   # → <platform-a-email@example.com>

# 确认 includeIf 是否生效
git config --show-origin user.name
# 应显示来自 ~/.gitconfig-<platform-a>
```

### 常见问题

**Q: includeIf 没生效？**

- 确保 `gitdir:` 路径末尾带 `/`
- 确保仓库路径匹配（区分大小写）
- 用 `git config --show-origin user.name` 查看当前值来源

**Q: 多平台如何管理凭据（密码/token）？**

- macOS: `osxkeychain` 按域名自动隔离，不同平台的 token 互不干扰
- Linux: 可用 `credential.helper` 按路径配置不同的存储文件
- 推荐优先使用 SSH 密钥代替密码

**Q: 已有仓库如何迁移？**

- 直接把仓库目录移动到 `~/workspace/multi-hub/<platform>/` 下即可

- 如果之前手动设过 `git config --local user.name`，清除后让 `includeIf` 接管：

  ```bash
  git config --local --unset user.name
  git config --local --unset user.email
  ```

### 文件结构总览

```
~/
├── .gitconfig                  # 全局：主代码仓身份 + includeIf 列表
├── .gitconfig-<platform-a>     # 平台 A 专属配置
├── .gitconfig-<platform-b>     # 平台 B 专属配置
├── .ssh/
│   ├── config                  # SSH 多密钥配置
│   └── id_ed25519_<platform>   # 各平台 SSH 密钥
└── workspace/
    ├── <main-platform-repos>/  # 主代码仓仓库（使用全局配置）
    └── multi-hub/
        ├── <platform-a>/       # 平台 A 仓库（自动切换身份）
        └── <platform-b>/       # 平台 B 仓库（自动切换身份）
```

---

## Git LFS

### 安装与初始化

```bash
# 安装 Git LFS（各平台包管理器）
brew install git-lfs          # macOS
apt install git-lfs           # Debian/Ubuntu
yum install git-lfs           # CentOS/RHEL

# 初始化（只需执行一次，全局生效）
git lfs install
```

### 追踪/取消追踪大文件

```bash
# 追踪指定模式的文件
git lfs track "*.psd"
git lfs track "*.zip"
git lfs track "*.so"
git lfs track "*.dll"

# 追踪单个文件
git lfs track "path/to/large-file.bin"

# 查看当前仓库的追踪规则
git lfs track

# 取消追踪
git lfs untrack "*.psd"
```

> `.gitattributes` 会自动追加追踪规则，需要和代码一起提交。

### 查看 LFS 文件状态

```bash
# 列出当前已用 LFS 管理的文件
git lfs ls-files

# 按文件大小排序
git lfs ls-files --size

# 查看最近一次提交的 LFS 文件
git lfs ls-files --all | tail -10

# 显示 LFS 指针文件的信息
git lfs pointer --file=path/to/file

# 查看当前暂存区的 LFS 状态
git lfs status
```

### 拉取和推送

```bash
# 拉取 LFS 文件（clone 后只拉指针，需 fetch 获取实际内容）
git lfs pull

# 拉取特定分支的 LFS 文件
git lfs fetch origin main

# 只拉取最近几次提交的 LFS 文件（节省空间）
git lfs fetch --recent

# 推送 LFS 文件（通常 git push 会自动触发）
git lfs push origin main --all
```

### 迁移已有仓库

```bash
# 将历史中已有的大文件迁移到 LFS（默认 --everything 覆盖全部分支）
git lfs migrate import --include="*.zip,*.tar.gz" --everything

# 只迁移特定分支
git lfs migrate import --include="*.so" --include-ref=main

# 先试运行，查看影响范围（不实际修改）
git lfs migrate info --include="*.zip" --everything
```

> `git lfs migrate` 会重写历史，执行前确保已备份或与团队协调。

### 克隆加速

```bash
# 克隆时跳过 LFS 文件下载（先拿到代码）
GIT_LFS_SKIP_SMUDGE=1 git clone <repo-url>

# 之后按需拉取
cd <repo>
git lfs pull
```

### 环境与维护

```bash
# 查看 LFS 配置信息（端点、存储路径等）
git lfs env

# 清理本地缓存的旧 LFS 文件（保留最近 3 天的）
git lfs prune

# 试运行，只展示会删除哪些文件
git lfs prune --dry-run --verbose

# 彻底删除远程不存在的 LFS 文件
git lfs prune --verify-remote
```
