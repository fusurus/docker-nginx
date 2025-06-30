# 更新环境

    apt update -y  && apt upgrade -y && apt install -y curl wget sudo socat

# 安装docker

    curl -fsSL https://get.docker.com | sh

# 创建nginx目录

    # 创建挂载目录
    mkdir -p /home/nginx/conf
    mkdir -p /home/nginx/log
    mkdir -p /home/nginx/html

## 容器中的nginx.conf文件和conf.d文件夹复制到宿主机

    # 生成容器
    docker run --name nginx -p 9001:80 -d nginx
    # 将容器nginx.conf文件复制到宿主机
    docker cp nginx:/etc/nginx/nginx.conf /home/nginx/conf/nginx.conf
    # 将容器conf.d文件夹下内容复制到宿主机
    docker cp nginx:/etc/nginx/conf.d /home/nginx/conf/conf.d
    # 将容器中的html文件夹复制到宿主机
    docker cp nginx:/usr/share/nginx/html /home/nginx/
