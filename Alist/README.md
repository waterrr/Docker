# Dockerfile for Alist
Original Author: https://github.com/Xhofe/alist  

Usage:  
1、使用前先按照要求修改conf.yml  参考链接:https://www.nn.ci/archives/alist.html  
2、运行命令，首次运行可能需要加载环境，需要一点时间，建议将下方3344改为127.0.0.1:3344并使用Nginx反代  

```
#Build it
docker build -f Dockerfile -t alist .

#Run it
docker run --restart=always -d -p 127.0.0.1:5244:5244 --name alist -v /opt/alist/conf.yml:/home/alist/conf.yml alist
```

Tips:  
本地数据持久化，如果需要修改配置先运行`docker stop alist`，然后直接修改目录下的`conf.yml`文件（无需进入容器），修改完成保存后`docekr start alist`  



### docker-compose.yml Coming Soon

