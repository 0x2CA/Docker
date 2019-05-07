FROM servicesdocker/alpinecn:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"

# 安装aria2
RUN   apk  update &&\
    apk  upgrade &&\
    apk add aria2

RUN mkdir -p ~/aria2 && mkdir -p ~/Downloads

WORKDIR /root/aria2

# 默认设置
add . /root/aria2

VOLUME [ "/root/aria2" ]

VOLUME [ "/root/Downloads" ]

EXPOSE 6800

CMD [ "/usr/bin/aria2c","--conf=aria2.conf"]



