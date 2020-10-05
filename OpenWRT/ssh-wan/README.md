# WAN에서 SSH 접속하기

기본적으로는 WAN에서 SSH 접속은 불가하고, LAN에서 접속은 가능

LAN에서 접속하는 주소는 192.168.1.1 (TP-LINK Archer c&, v5)

WAN에서 접속하려면:
1. https://gist.github.com/lynus/3446706
2. add the following lines in /etc/config/firewall :

config rule
    option src              wan
    option dest_port        22
    option target           ACCEPT
    option proto            tcp 

after restart ('reboot' commmand),wrt accept port 22 request (in this case ,ssh request)from wan.

위의 방법을 통해서, WAN에서 OpenWRT SSH 접속이 가능했음.