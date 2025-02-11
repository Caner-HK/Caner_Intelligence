### Caner Intelligence

> [!WARNING]
> 本仓库的改动过多，[原文档](https://github.com/Caner-HK/Caner_Intelligence/blob/main/README.OI.md)部分内容已不再适用，请以本文档为准！

-----
#### 使用 Docker
首先，你需要是本组织内成员才有权限拉取。
> [!IMPORTANT]
> 由于本仓库镜像未公开，在`docker pull`之前需要登录（参照[官方文档](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-with-a-personal-access-token-classic)），因此一切`ghcr.io`镜像站均无法使用，请自行代理！

1.参照[官方文档](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-with-a-personal-access-token-classic)登录
> [!IMPORTANT]
> 如果使用`sudo`拉取，请确保登录时也是`root`用户，否则无法正常拉取！

2.使用以下命令拉取镜像
```bash
docker pull ghcr.io/caner-hk/caner_intelligence:latest
```

3.启动！
```bash
docker run -d -p 3000:8080 -e OLLAMA_BASE_URL=https://example.com -v open-webui:/app/backend/data --name ci --restart always ghcr.io/caner-hk/caner_intelligence:latest
```

*未完待续*