FROM cdegroot/rpi-alpine:3.2.3
MAINTAINER Cees de Groot <casedeg@gmail.com>

RUN cd /tmp && \
    apk --update add wget ca-certificates && \
    wget --no-check-certificate https://dl.dropboxusercontent.com/u/2187136/otp_19.0_armv7_musl.tar.gz && \
    cd / && \
    tar xvfz /tmp/otp_19.0_armv7_musl.tar.gz && \
    rm /tmp/otp_19.0_armv7_musl.tar.gz && \
    rm -rf /var/cache/apk/*

CMD ["/bin/sh"]
