FROM cdegroot/rpi-alpine:3.2.3
MAINTAINER Cees de Groot <casedeg@gmail.com>

ENV REFRESHED_AT 20160716-1711Z

RUN cd /tmp && \
    apk --update add wget ca-certificates && \
    wget -nv --no-check-certificate https://dl.dropboxusercontent.com/u/2187136/rpi-otp/otp_19.0_armv7_musl.tar.gz && \
    cd / && \
    tar xvfz /tmp/otp_19.0_armv7_musl.tar.gz && \
    rm /tmp/otp_19.0_armv7_musl.tar.gz && \
    rm -rf /var/cache/apk/*

CMD ["/bin/sh"]
