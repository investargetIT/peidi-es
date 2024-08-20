# 测试环境部署
1. 使用 Maven 打包生成 jar 文件
2. 删除旧的镜像
2. 构建 Docker 镜像 `docker build -t peidi-es .`
3. 导出镜像到本地 `docker save -o peidi-es.tar peidi-es`
4. 上传镜像到远程服务器
5. 远程服务器上载入镜像 `docker load -i peidi-es.tar`
6. 停止并移除旧的容器 `docker stop peidi-es` `docker rm peidi-es`
7. 运行新的容器 `docker run --name peidi-es -p 8084:8084 -d peidi-es`
