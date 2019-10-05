FROM docker.pkg.github.com/seankhliao/archrepo/base-devel:latest

RUN pacman -S --noconfirm --noprogressbar git && \
    useradd -m user
RUN git clone https://aur.archlinux.org/yay.git && \
    cd yay && \
    makepkg -si --noconfirm --noprogressbar && \
    cd .. && \
    rm -rf yay
USER user
