#
# Mr.z
#

FROM archlinux/base:latest

# 作者信息
MAINTAINER servicedocker "2478557459@qq.com"

# 拷贝
COPY . /
# 跟新系统
RUN   pacman -Syu 

# key更新
RUN pacman-key --init && \
    pacman-key --populate archlinux  && \
    pacman  -Sy  --noconfirm archlinuxcn-keyring 

# 安装yaourt
RUN  pacman -Sy --noconfirm  yaourt 

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
    nvm install 10.15.3 &&\
    nvm use 10.15.3 

CMD [ "/bin/bash" ]

