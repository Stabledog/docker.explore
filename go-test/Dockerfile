FROM golang

RUN apt update && apt install \
    vim-tiny \
    -y \
    && cd /usr/bin && ln vi vim

WORKDIR /root
COPY bashrc-root .bashrc
COPY profile-root .profile

ENTRYPOINT [ "/bin/bash" , "-l"]
