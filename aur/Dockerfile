FROM docker.pkg.github.com/seankhliao/archrepo/base-devel:latest

RUN pacman -S --noconfirm --noprogressbar git && \
    useradd -m user && \
    echo "user ALL=NOPASSWD: ALL" >> /etc/sudoers

USER user
WORKDIR /home/user
RUN git clone https://aur.archlinux.org/yay-bin.git && \
    cd yay-bin && \
    makepkg -si --noconfirm --noprogressbar && \
    cd .. && \
    rm -rf yay-bin
