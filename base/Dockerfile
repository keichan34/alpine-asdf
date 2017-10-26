FROM alpine:latest
MAINTAINER Keitaroh Kobayashi <keita@kbys.me>

RUN apk add --no-cache git curl alpine-sdk openssl-dev zip unzip dpkg-dev openssh-client \
    ca-certificates bash gnupg perl-utils

ENV PATH="/root/.asdf/shims:/root/.asdf/bin:${PATH}"

RUN git clone --depth 1 --branch v0.4.0 https://github.com/asdf-vm/asdf.git $HOME/.asdf && \
    echo '. $HOME/.asdf/asdf.sh' >> $HOME/.bashrc && \
    echo '. $HOME/.asdf/asdf.sh' >> $HOME/.profile

