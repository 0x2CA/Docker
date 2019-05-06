FROM alpine:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"

# 更新源
RUN   echo https://mirrors.aliyun.com/alpine/latest-stable/main >/etc/apk/repositories &&\
    echo https://mirrors.aliyun.com/alpine/latest-stable/community >>/etc/apk/repositories 

# 更新系统
Run apk  upgrade &&\
    apk  update


