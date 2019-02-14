
## 服务端搭建

Debian/Ubuntu:
```bash
apt-get install python-pip
pip install shadowsocks

ssserver -p 443 -k password -m rc4-md5
sudo ssserver -p 443 -k password -m rc4-md5 --user nobody -d start  # run as daemon
sudo ssserver -d stop
tail -f /var/log/shadowsocks.log
```

[相关链接](https://github.com/shadowsocks/shadowsocks/wiki/Shadowsocks-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E)




