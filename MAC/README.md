
## 清理MAC系统空间
1. 删除 /cores 下的所有文件， 也可以 在(没有就新建)/etc/sysctl.cof中添加 kern.coredump=1 不让core文件生成

2. 删除docker qcow2 文件
```
docker rm $(docker ps -a -q)
docker rmi $(docker images -q)
docker volume rm $(docker volume ls |awk '{print $2}')
rm -rf ~/Library/Containers/com.docker.docker/Data/*
```
