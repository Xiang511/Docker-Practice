# Docker-Practice
練習 Docker

[20 分鐘入門 Docker，建立屬於你自己的 Docker Image｜六角學院｜2023 鐵人賽 #23](https://www.youtube.com/watch?v=RsY5cCc9RGM)  


[運行 Docker 在 Ubuntu 環境｜從本地端上傳 Docker Image 至 Ubuntu 伺服器｜六角學院｜2023 鐵人賽 #24](https://www.youtube.com/watch?v=JocSDHOFNzw)  

[超容易！10 分鐘透過 Docker hub 部署 image｜六角學院｜2023 鐵人賽 #25](https://www.youtube.com/watch?v=hxX5MIohy1Q&t=537s)

```bash
docker build -t express-mvc .
# 建立名為 express-mvc 的 Docker Image

docker build --platform=linux/amd64 -t express-mvc-linux .
# 建立名為 express-mvc 的 Docker Image (for linux/amd64 架構 )

docker save -o express-mvc.tar express-mvc
#此命令將名為 express-mvc 的 Docker 映像檔保存為 express-mvc.tar 檔案

docker images
# 列出所有的 Docker Images

docker rmi express-mvc
# 刪除名為 express-mvc 的 Docker Image

docker run -p 3005:3000 -d express-mvc
# 在背景運行名為 express-mvc 的容器，並將本地端的 3005 埠映射到容器的 3000 埠

docker ps -a
# 列出所有的容器，包括運行中的和停止的

docker stop 75da352166b1
# 停止容器 ID 為 75da352166b1 的容器

docker start 75da352166b1
# 啟動容器 ID 為 75da352166b1 的容器

docker rm 75da352166b1
# 刪除容器 ID 為 75da352166b1 的容器


docker tag express-mvc hsiang511/docker-practice:express-mvc
# 將名為 express-mvc 的 Docker Image 標記為 hsiang511/docker-practice:express-mvc

docker push hsiang511/docker-practice:express-mvc
# 將標記為 hsiang511/docker-practice:express-mvc 的 Docker Image 推送到 Docker Hub

docker pull hsiang511/docker-practice:express-mvc
# 從 Docker Hub 拉取標記為 hsiang511/docker-practice:express-mvc 的 Docker Image


```
