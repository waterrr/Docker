FROM ubuntu:20.04
LABEL maintainer="admin@gksec.com"

COPY conf.yml /home/Alist/conf.yml
ADD alist_0.1.6_linux_amd64.tar.gz /home/Alist/
ADD refs.tags.v0.1.7.tar.gz /home/Alist/

WORKDIR /home/Alist/

EXPOSE 5244

CMD chmod +x alist \
	&&apt update \
	&&apt install -y ca-certificates \
    &&./alist > log.log 2>&1