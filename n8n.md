在 docker 根目录新建文件夹
mkdir -p n8n_data
然后运行一下 docker 命令建立 docker
docker run -d --name n8n --restart unless-stopped -p 5678:5678 -v ./n8n_datan8n_data:/home/node/.n8n n8nio/n8n
