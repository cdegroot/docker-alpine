FROM cdegroot/rpi-elixir:1.3.1
MAINTAINER Cees de Groot <casedeg@gmail.com>

ENV REFRESHED_AT 20160716-1722Z

RUN cd /tmp; for i in \
    asn1-4.0.3 \
    crypto-3.7 \
    megaco-3.18.1 \
    sasl-3.0 \
    common_test-1.12.2 \
    diameter-1.12 \
    mnesia-4.14 \
    snmp-5.2.3 \
    compiler-7.0 \
    edoc-0.7.19 \
    observer-2.2 \
    ssh-4.3 \
    cosEvent-2.2.1 \
    cosEventDomain-1.2.1 \
    eldap-1.2.2 \
    ssl-8.0 \
    cosEventDomain-1.2.1 \
    erl_interface-3.9 \
    orber-3.8.2 \
    stdlib-3.0 \
    cosFileTransfer-1.2.1 \
    diameter-1.12 \
    et-1.6 \
    inets-6.3 \
    parsetools-2.1.2 \
    os_mon-2.4.1 \
    syntax_tools-2.0 \
    cosNotification-1.2.2 \
    eunit-2.3 \
    otp_mibs-1.1.1 \
    cosProperty-1.2.1 \
    cosNotification-1.2.2 \
    ic-4.4.1 \
    public_key-1.2 \
    parsetools-2.1.2 \
    xmerl-1.3.11 \
    cosTime-1.2.2 \
    inets-6.3 \
    public_key-1.2 \
    cosTransactions-1.3.2 \
    kernel-5.0 \
    runtime_tools-1.10; \
    do \
      wget -nv --no-check-certificate https://dl.dropboxusercontent.com/u/2187136/rpi-otp/${i}_armv7l_musl.tar.gz && \
      (cd /usr/local/lib/erlang/lib; tar xfz /tmp/${i}*tar.gz; rm /tmp/${i}*tar.gz); \
    done && \
    apk --update add git && \
    rm -rf /etc/ssl && \
    rm -rf /var/cache/apk/*

RUN mix local.hex --force && \
    mix local.rebar --force

CMD ["/bin/sh"]
