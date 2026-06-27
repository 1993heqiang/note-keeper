# Docker 脚本与命令

## 常用命令

### 镜像

```shell
# 拉取镜像
docker pull <image>:<tag>

# 列出本地镜像
docker images

# 删除镜像
docker rmi <image>

# 构建镜像（-f 指定 Dockerfile）
docker build -f deploy/Dockerfile -t <name>:<tag> .

# 交叉编译（ARM 机器上构建 x86 镜像）
docker buildx build -f deploy/Dockerfile --platform linux/amd64 -t <name>:<tag>-amd64 .

# 交叉编译（x86 机器上构建 ARM 镜像）
docker buildx build -f deploy/Dockerfile --platform linux/arm64 -t <name>:<tag>-arm64 .

# 导出镜像（本地 → 服务器）
docker save -o <name>.tar <name>:<tag>

# 导入镜像（在服务器上执行）
docker load -i <name>.tar

# 打标签
docker tag <src> <dst>

# 清理悬空镜像（无标签的中间层）
docker image prune

# 清理所有未使用的镜像
docker image prune -a
```

### 容器

```shell
# 列出运行中的容器
docker ps

# 列出所有容器（含已停止）
docker ps -a

# 运行容器（-d 后台 / -p 端口映射 / -v 挂载 / --name 命名 / --restart 重启策略）
docker run -d --name <name> -p 8080:80 -v /host:/container <image>

# 进入容器
docker exec -it <container> bash

# 启动 / 停止 / 重启
docker start <container>
docker stop <container>
docker restart <container>

# 删除容器
docker rm <container>

# 查看日志
docker logs -f <container>

# 文件复制（宿主机 → 容器）
docker cp <src> <container>:<dst>

# 查看容器详情（挂载、网络、环境变量等）
docker inspect <container>

# 输出完整 docker run 命令
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock \
  assaflavie/runlike <container>
```

### Compose

```shell
# 启动（-d 后台）
docker compose up -d

# 停止并清理
docker compose down

# 查看状态
docker compose ps

# 查看日志
docker compose logs -f

# 重启服务
docker compose restart

# 更新镜像并重新部署
docker compose pull && docker compose up -d

# 当前 docker-compose 项目的运行路径（所在文件夹）
docker compose ls
```

### 系统

```shell
# 查看磁盘占用
docker system df

# 全面清理（停止的容器 + 未使用的网络 + 悬空镜像 + 构建缓存）
docker system prune

# 查看数据卷
docker volume ls

# 清理未使用的数据卷
docker volume prune

# 查看网络
docker network ls
```

## 配置

> 配置文件：`/etc/docker/daemon.json`，修改后需重启 Docker 生效。

### 代理

```shell
# 编辑 daemon.json
sudo vim /etc/docker/daemon.json
```

```json
{
  "proxies": {
    "http-proxy": "http://proxy.example.com:8080",
    "https-proxy": "http://proxy.example.com:8080",
    "no-proxy": "localhost,127.0.0.1,.local"
  }
}
```

### 镜像加速

```json
{
  "registry-mirrors": ["https://docker.1ms.run", "https://docker.xuanyuan.me"]
}
```

### 重启生效

```shell
# 配置变更后重载并重启
sudo systemctl daemon-reload
sudo systemctl restart docker

# 验证配置已生效
docker info | grep -A 5 "Registry Mirrors"
```

## 服务部署

### QwenClaw

```bash
docker run -d --name ali-qwenpaw \
  -p 127.0.0.1:8088:8088 \
  -v ~/workspace/docker-data/qwenpaw/qwenpaw-data:/app/working \
  -v ~/workspace/docker-data/qwenpaw/qwenpaw-secrets:/app/working.secret \
  -v ~/workspace/docker-data/qwenpaw/qwenpaw-backups:/app/working.backups \
  --env-file ~/workspace/docker-data/qwenpaw/.env \
  agentscope/qwenpaw:v1.1.9
```

`.env`文件配置:

```bash
QWENPAW_AUTH_ENABLED=true
QWENPAW_AUTH_USERNAME=admin
QWENPAW_AUTH_PASSWORD=xxxx
TZ=Asia/Shanghai
```

### linuxserver/firefox

```bash
# 一键启动（中文+无乱码）
docker run -d \
  --name=firefox \
  -p 3001:3001 \
  -p 3000:3000 \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Asia/Shanghai \
  -e LANG=zh_CN.UTF-8 \
  -e LC_ALL=zh_CN.UTF-8 \
  -e FIREFOX_CLI=https://www.google.com/  \
  -e DOCKER_MODS=linuxserver/mods:universal-package-install \
  -e INSTALL_PACKAGES=fonts-noto-cjk \
  -v ~/workspace/docker-data/firefox-config:/config \
  --shm-size=2g \
  --restart unless-stopped \
  linuxserver/firefox:latest
```
