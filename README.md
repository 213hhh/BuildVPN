# BuildVPN



yum -y install wget    #ContOS 安装 wget
yum -y install curl    #ContOS 安装 curl
//bbrplus加速
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
//安装docker
yum install docker -y
//启动docker
service docker start
//安装ssr
docker pull oddrationale/docker-shadowsocks
//启动服务
docker run -d -p 2020:2020 oddrationale/docker-shadowsocks -s 0.0.0.0 -p 2020 -k wxy19981207 -m aes-256-cfb
//查看开放端口
netstat -ltnp
netstat -anp
