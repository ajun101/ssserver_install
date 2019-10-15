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
thanks to the author of ss.sh.
input:
wget -O ss.sh https://github.com/ajun101/ssserver_install/blob/master/ss.sh
chmod u+x ss.sh
./ss.sh
then follow the guide
