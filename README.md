# ssserver_install
support centos 7
1. install bbr
input: 
wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh
chmod u+x bbr.sh
./bbr.sh
2. check bbr
input: 
sysctl net.ipv4.tcp_congestion_control
ouput:
net.ipv4.tcp_congestion_control = bbr
3. install ssserver
input:
wget -O ss.sh http://45.32.195.77/file/ss.sh
chmod u+x ss.sh
./ss.sh
then follow the guide
