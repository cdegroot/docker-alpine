FROM cdegroot/rpi-erlang:19.0
MAINTAINER Cees de Groot <casedeg@gmail.com>

ENV REFRESHED_AT 20160716-1717Z

ENV ELIXIR_VERSION 1.3.1

RUN apk --update add --virtual build-dependencies wget ca-certificates && \
    wget -nv --no-check-certificate https://github.com/elixir-lang/elixir/releases/download/v${ELIXIR_VERSION}/Precompiled.zip && \
    mkdir -p /opt/elixir-${ELIXIR_VERSION}/ && \
    unzip Precompiled.zip -d /opt/elixir-${ELIXIR_VERSION}/ && \
    rm Precompiled.zip && \
    apk del build-dependencies && \
    rm -rf /etc/ssl && \
    rm -rf /var/cache/apk/*

ENV PATH $PATH:/opt/elixir-${ELIXIR_VERSION}/bin

CMD ["/bin/sh"]
