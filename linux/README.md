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
