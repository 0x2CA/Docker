FROM servicesdocker/archlinuxcn:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"


# 更新系统
RUN   yaourt -Syu 

# 安装nvm
RUN  yaourt -Sy --noconfirm  nvm &&  \
    yaourt -Sy --noconfirm grep &&\
    yaourt -Sy --noconfirm awk &&\
    echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.bashrc &&\
    echo 'source /usr/share/nvm/init-nvm.sh' >> ~/.zshrc 

# 安装node 
RUN  [ -z "$NVM_DIR" ] && export NVM_DIR="$HOME/.nvm"  &&\
    source /usr/share/nvm/nvm.sh &&\
    source /usr/share/nvm/bash_completion &&\
    source /usr/share/nvm/install-nvm-exec &&\
    yaourt -Sy --noconfirm tar &&\
    nvm install `nvm  ls-remote --lts |grep -P -o  v[0-9]+.[0-9]+.[0-9]+ | tail -1 ` &&\
    nvm use `nvm  ls-remote --lts |grep -P -o  v[0-9]+.[0-9]+.[0-9]+ | tail -1 `

CMD [ "/bin/bash" ]

