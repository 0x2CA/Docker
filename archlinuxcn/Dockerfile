FROM archlinux/base:latest

# 作者信息
MAINTAINER servicesdocker "2478557459@qq.com"

# 源更新
RUN  curl -o /etc/pacman.d/mirrorlist https://www.archlinux.org/mirrorlist/?country=CN  &&\
    sed  -i 's/#Se/Se/g' /etc/pacman.d/mirrorlist &&\
    echo "" >> /etc/pacman.conf &&\
    echo "[archlinuxcn]" >> /etc/pacman.conf &&\
    echo "#The Chinese Arch Linux communities packages." >> /etc/pacman.conf &&\
    echo "SigLevel = Optional TrustedOnly" >> /etc/pacman.conf &&\
    echo "Server   = http://repo.archlinuxcn.org/$arch" >> /etc/pacman.conf

# 更新系统
RUN   pacman -Syu 

# key更新
RUN pacman-key --init && \
    pacman-key --populate archlinux  && \
    pacman  -Sy  --noconfirm archlinuxcn-keyring 

# 安装yaourt
RUN  pacman -Sy --noconfirm  yaourt 

CMD [ "/bin/bash" ]
