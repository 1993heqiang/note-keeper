# Linux 常用命令

## 端口与进程

### 找端口

```shell
# 查看端口被哪个进程占用
lsof -i :<port>
ss -tlnp | grep <port>

# 查看所有监听端口
ss -tlnp

# 查看某个进程占用的端口
lsof -p <pid> | grep LISTEN
```

### 杀进程

```shell
# 按端口杀进程
kill -9 $(lsof -t -i:<port>)

# 按进程名查找
ps aux | grep <name>

# 杀指定 PID
kill -9 <pid>

# 批量按名称杀
pkill -9 -f <name>

# 优雅终止（SIGTERM）
kill <pid>

# 后台运行并忽略 HUP 信号
nohup <command> >> nohup.log 2>&1 &
```

## 文件与磁盘

```shell
# 查看磁盘使用
df -h

# 查看目录大小
du -sh <dir>

# 按大小排序列出当前目录下所有文件/子目录
du -sh * | sort -rh

# 查找文件
find <dir> -name "<pattern>"

# 查看文件行数
wc -l <file>

# 实时查看文件末尾
tail -f <file>
```

## 系统信息

```shell
# 系统版本
cat /etc/os-release
uname -a

# 内存使用
free -h

# CPU 信息
lscpu
nproc
```

## 网络

```shell
# 查看网络接口
ip a

# 测试连通性
ping <host>

# DNS 解析
nslookup <domain>
dig <domain>

# 下载文件
curl -O <url>
wget <url>
```

## 用户与权限

```shell
# 修改文件所有者
chown <user>:<group> <file>

# 修改文件权限
chmod 755 <file>
chmod +x <script>

# 切换用户
su - <user>

# 以 root 执行命令
sudo <command>
```
