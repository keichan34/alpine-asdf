FROM keichan34/alpine-asdf:base
MAINTAINER Keitaroh Kobayashi <keita@kbys.me>

RUN apk add --no-cache ncurses-dev

RUN curl https://raw.githubusercontent.com/kerl/kerl/master/kerl > /usr/local/bin/kerl && \
    chmod +x /usr/local/bin/kerl

RUN asdf plugin-add erlang https://github.com/eproxus/asdf-kerl && \
    asdf plugin-add elixir && \
    asdf plugin-add nodejs

RUN bash ~/.asdf/plugins/nodejs/bin/import-release-team-keyring

ARG NODEJS_VERSION
ENV NODEJS_VERSION $NODEJS_VERSION
RUN asdf install nodejs $NODEJS_VERSION

ARG ERLANG_VERSION
ENV ERLANG_VERSION $ERLANG_VERSION
RUN asdf install erlang $ERLANG_VERSION

ARG ELIXIR_VERSION
ENV ELIXIR_VERSION $ELIXIR_VERSION
RUN asdf install elixir $ELIXIR_VERSION

