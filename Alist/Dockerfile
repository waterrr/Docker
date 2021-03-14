FROM ubuntu:20.04
LABEL maintainer="admin@gksec.com"

COPY conf.yml /home/alist/conf.yml
ADD alist_1.0.0_linux_amd64.tar.gz /home/alist/
ADD refs.tags.v1.0.0.tar.gz /home/alist/

WORKDIR /home/alist/

EXPOSE 5244

CMD sed -i "s/archive.ubuntu.com/mirrors.aliyun.com/g" /etc/apt/sources.list \
	  &&apt update \
	  &&apt install -y ca-certificates \
    	  &&./alist > log.log 2>&1
