#
# Mr.z
#

FROM servicesdocker/archlinuxcn:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"

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
    nvm install 10.15.3 &&\
    nvm use 10.15.3 

CMD [ "/bin/bash" ]

