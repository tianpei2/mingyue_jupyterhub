# linux

## 1. ps bash
```
ps aux | grep configurable-http-proxy
```

```
netstat -tunlp
```

```
ps -aux | grep jupyter
```

## 2. 远程连接windows
在linux下面创建一个需要挂载到的目录
```
/usr/local/bin/code
```

利用`mount`命令进行挂载
```
mount -t cifs -o username=Bob,password=123456 //192.168.0.102/Share /usr/local/bin/code
```

## 3. 本地文件上传linux
```
scp /download/index.html root@39.97.235.240:/var/www/html
# 该命令将本地 /download 目录下 index.html 上传至 39.97.235.240 服务器 root 用户下 /var/www/html 目录
```
## 4. 创建linux用户
```
useradd -d "/home/tianpei" -m -s "/bin/bash" tianpei
```

`-d "/home/tt"`：就是指定`/home/tt`为主目录

`-m` 就是如果`/home/tt`不存在就强制创建

`-s` 就是指定`shell`版本
