FROM archlinux/base


RUN pacman -Sy --noconfirm --noprogressbar reflector && \
    reflector --latest 5 --sort rate --save /etc/pacman.d/mirrorlist
RUN pacman -Syu --noconfirm --noprogressbar base-devel
