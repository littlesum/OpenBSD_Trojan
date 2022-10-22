# OpenBSD-Trojan-X86-bin
# 这是一个源于trojan-gfw的OpenBSD预编译版本，以及一个运行需要的rc.d 简单脚本，仅仅能保证服务运行！

## trojan-openbsd-x86_64 是预编译可执行文件

## 使用说明

## OpenBSD 更新7.2 所以更新预编译文件到7.2

1. Download files
2. cp （bin file） to dir /usr/bin/
3. mkdir /etc/trojan
4. create your trojan config file 
5. cp trojan to /etc/rc.d 
6. chmod +x /etc/rc.d/trojan
7. rcctl enable trojan #boot enable your trojan service
8. rcctl start trojan #start your trojan service
