FROM docker.pkg.github.com/seankhliao/archrepo/base-devel:latest

RUN pacman -S --noconfirm --noprogressbar git && \
    useradd -m user && \
    echo "user ALL=NOPASSWD: ALL" >> /etc/sudoers

USER user
WORKDIR /home/user
RUN git clone https://aur.archlinux.org/yay-bin.git && \
    makepkg -si --noconfirm --noprogressbar -p yay-bin/PKGBUILD && \
    rm -rf yay-bin
