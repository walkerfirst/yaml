在 docker 根目录新建文件夹
mkdir -p n8n_data
然后运行一下 docker 命令建立 docker
docker run -d --name n8n --restart unless-stopped -p 5678:5678 -v ./n8n_datan8n_data:/home/node/.n8n n8nio/n8n

如果遇到 command start not found 是因为自定义的文件夹 /volume1/docker 权限不够.

请重新用如下命令

1. 停止并删除现有容器

docker stop n8n

docker rm n8n

2. 修复目录权限
   sudo chown -R 1000:1000 /volume1/docker/n8n
   sudo chmod -R 755 /volume1/docker/n8n
