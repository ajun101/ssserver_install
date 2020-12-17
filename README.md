# ssserver_install
support centos 7
1. install bbr <br/>
input: <br/>
wget --no-check-certificate https://github.com/teddysun/across/raw/master/bbr.sh <br/>
chmod u+x bbr.sh <br/>
./bbr.sh <br/>
2. check bbr <br/>
input: <br/>
sysctl net.ipv4.tcp_congestion_control <br/>
ouput: <br/>
net.ipv4.tcp_congestion_control = bbr <br/>
3. install ssserver <br/>
thanks to the author of ss.sh. <br/>
input: <br/>
wget -O ss.sh https://github.com/ajun101/ssserver_install/raw/master/ss.sh <br/>
chmod u+x ss.sh <br/>
./ss.sh <br/>
then follow the guide <br/>


3.install Trojan instead<br/>
thanks to the author of Trojan.sh<br/>
input: <br/>
wget -O trojan_centos7.sh https://github.com/atrandys/trojan/raw/master/trojan_centos7.sh <br/>
or wget https://github.com/V2RaySSR/Trojan/raw/master/Trojan.sh <br/>
<br/>
project address: https://github.com/atrandys/trojan <br/>
chrome plugin: https://github.com/FelisCatus/SwitchyOmega/releases <br/>
gfwlist: https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt<br/>

update https cert
acme.sh --issue -d tj.friends-game.top --webroot /usr/share/nginx/html/ --force
acme.sh --installcert -d tj.friends-game.top --key-file /usr/src/trojan-cert/private.key --fullchain-file /usr/src/trojan-cert/fullchain.cer --reloadcmd "systemctl force-reload nginx.service"
systemctl stop trojan
systemctl start trojan
