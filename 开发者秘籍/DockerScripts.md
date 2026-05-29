### CoClaw

```bash
docker run -d --name ali-qwenpaw \
  -p 127.0.0.1:8088:8088 \
  -v ~/workspace/docker-data/qwenpaw/qwenpaw-data:/app/working \
  -v ~/workspace/docker-data/qwenpaw/qwenpaw-secrets:/app/working.secret \
  -v ~/workspace/docker-data/qwenpaw/qwenpaw-backups:/app/working.backups \
  --env-file ~/workspace/docker-data/qwenpaw/.env \
  agentscope/qwenpaw:v1.1.2
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
