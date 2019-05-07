FROM servicesdocker/alpinecn:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"

# 安装aria2
RUN   apk  update &&\
    apk  upgrade &&\
    apk add --no-cache aria2 git darkhttpd &&\
    git clone --depth=1 https://github.com/ziahamza/webui-aria2 /tmp/webui-aria2 && \
    mkdir /aria2-webui &&\
    cp -r /tmp/webui-aria2/docs/* /aria2-webui/ &&\
    rm -rf /tmp/* &&\
    apk del git 

# 默认设置
ADD . /

RUN mkdir -p /data &&\
    chmod +x /usr/bin/aria2d &&\
    chmod +x /usr/bin/trackers-list-aria2 &&\
    dos2unix /usr/bin/aria2d &&\
    dos2unix /usr/bin/trackers-list-aria2

WORKDIR /conf

VOLUME [ "/conf"]

VOLUME [ "/data" ]

EXPOSE 6800

EXPOSE 80

CMD [ "/usr/bin/aria2d"]



