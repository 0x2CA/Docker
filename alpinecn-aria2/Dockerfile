FROM servicesdocker/alpinecn:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"

# 安装aria2
RUN   apk  update &&\
    apk  upgrade &&\
    apk add --no-cache aria2 darkhttpd &&\
    wget https://github.com/mayswind/AriaNg-DailyBuild/archive/master.zip -O /tmp/ariang.zip &&\
    mkdir /aria2-webui &&\
    unzip /tmp/ariang.zip &&\
    cp -r /AriaNg-DailyBuild-master/* /aria2-webui/ &&\
    rm -rf /tmp/* &&\
    rm -rf /AriaNg-DailyBuild-master

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



