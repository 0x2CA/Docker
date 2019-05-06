FROM servicesdocker/alpinecn:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"

# 安装nvm、编译最新node-lts
RUN apk  update &&\
    apk  upgrade &&\
    apk add --no-cache curl ca-certificates openssl ncurses coreutils python2 make gcc g++ libgcc linux-headers grep util-linux binutils findutils &&\
    curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash &&\
    export NVM_DIR="$HOME/.nvm" &&\
    [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  &&\
    nvm  install  -s `nvm  ls-remote --lts |grep -P -o  v[0-9]+.[0-9]+.[0-9]+ | tail -1 ` &&\
    nvm use `nvm  ls-remote --lts |grep -P -o  v[0-9]+.[0-9]+.[0-9]+ | tail -1 `





