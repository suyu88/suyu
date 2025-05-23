# suyu
# 这里使用的是unbuntu 22.04版本系统
# 查看IP
ip add
# 测试网络
ping www.baidu.com
# 配置网络，以及远程连接端口
vi /etc/netplan/50-cloud-init.yaml
netplan apply
vi /etc/ssh/sshd_config
service sshd restart
# 防火墙检查以及放行端口
service firewalld status
systemctl status firewalld
systemctl status iptable
service ssh restart
ufw status
vi /etc/ssh/sshd_config
# 允许系统响应 ICMP 回显请求
sysctl net.ipv4.icmp_echo_ignore_all=0
# 防火墙状态
ufw status
ufw enable
ufw status
# 放行远程端口22 和 48568 (自用)
ufw allow 22/tcp
ufw allow 22/udp
vi /etc/ssh/sshd_config
systemctl restart sshd
ufw allow 48568/tcp
ufw allow 48568/udp
ufw reload
# 更新各类依赖安装包
apt-get update
apt upgrade -y
sudo apt update && sudo apt upgrade -y
# 1.网络下载ssr 安装脚本(网载，授权，运行，授权前看白色文件，授权后是绿色文件)
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev.sh
ls 
chmod +x shadowsocks-libev.sh
ls
./shadowsocks-libev.sh
bash shadowsocks-libev.sh
# 2.网络下载ssr 安装脚本(网载，授权，运行，授权前看白色文件，授权后是绿色文件)
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
./shadowsocks-all.sh

# 3.进行3x-ui 网载并运行，按照要求设置web页面远程面板端口和账号密码
bash <(curl -Ls https://raw.githubusercontent.com/mhsanaei/3x-ui/master/install.sh)
# 运行并设置登录信息以及端口
x-ui

# x-ui 面板端口
ufw allow 8088/tcp
ufw allow 8088/udp
# 网载安装 bbr 加速
bash <(curl -s https://raw.githubusercontent.com/opiran-club/VPS-Optimizer/main/bbrv3.sh --ipv4)
uname -r
lsmod | grep bbr
ufw allow 443/tcp
ufw allow 443/udp
x-ui
reboot
x-ui
13
x-ui
ufw allow 11246/tcp
ufw allow 11246/udp
ip add
history
ls
x-ui
ip add
ping 43.250.184.165
ping 43.250.184.167
vi /etc/netplan/50-cloud-init.yaml
netplan apply
ip add
ls
ip add
systemctl firewalld status
systemctl status firewalld
systemctl status ufw
ufw status
ufw status numbered
ufw delete
ufw status numbered
ufw delete 7
ufw status numbered
ufw delete 7
ufw reload
ufw status
ufw allow verbose
ufw status verbose
ufw status numbered
ufw delete 13 14
ufw status numbered
ufw delete 13
ufw status
ufw status numbered
ufw allow 29275/tcp
ufw allow 29275/udp
ufw reload
service restart ufw
service ufw restart
ufw status
ip add
x-ui
ssh root@45.61.236.183 -p 48568
ssh root@45.61.236.183
vi /etc/ssh/sshd_config
ufw status
exit
ip add
ip ad
ip add
curl http://update.yk2004.com/cdn20/2.33/nginx-2-33/ants_agent/ants_agent
curl -O http://update.yk2004.com/cdn20/2.33/nginx-2-33/ants_agent/ants_agent
ip add
ssh root@45.61.225.112
ping 45.61.225.112 -t
ping 45.61.225.112
ip add
cat /etc/issue
history
