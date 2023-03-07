### 一、在有互联网的设备安装代理.
```javascript
yum install squid -y
vi /etc/squid/squid.conf
acl localnet src 172.27.0.0/24    #授权的网段
http_port 3128   #端口
http_access allow localnet    #开启授权
systemctl start squid
```

### 一、在没有互联网的服务器执行
```javascript
export http_proxy=http://x.x.x.x:3128/    #有互联网服务器的IP
```
