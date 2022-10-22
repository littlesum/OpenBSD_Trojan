# OpenBSD-Trojan-X86-bin
# 这是一个源于[trojan-gfw](https://github.com/trojan-gfw/trojan)的OpenBSD预编译版本，以及一个运行需要的rc.d 简单脚本，仅仅能保证服务运行！

## trojan-openbsd-x86_64 openbsd 7.1 的预编译可执行文件

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

# OpenBSD 7.2 building progress 
1. first download sources 
2. install Dependencies lib
**pkg_add boost cmake openssl
3. configure cmake
```cmake -DCMAKE_INSTALL_PREFIX=/usr/bin/trojan \
      -DOPENSSL_ROOT_DIR=/usr/local \
      -DOPENSSL_INCLUDE_DIR=/usr/local/include \
      -DOPENSSL_SSL_LIBRARY=/usr/lib/libssl.so.52.0 \
      -DOPENSSL_CRYPTO_LIBRARY=/usr/lib/libcrypto.so.50.0 \
      -DENABLE_MYSQL=OFF \
      --trace --debug-output```
      
***without no mysql support
 4. make
```make install```
 or 
 ```make``` && ```cp trojan /usr/bin```
 5. mkdir /etc/trojan
 6. config trojan
 7. done
