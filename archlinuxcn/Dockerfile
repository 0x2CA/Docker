#
# Mr.z
#

FROM archlinux/base:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"

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

CMD [ "/bin/bash" ]
