FROM ubuntu:14.04
MAINTAINER Vinicius Silva <viniicius.conceicao@gmail.com>

RUN apt-get update && apt-get install -y --no-install-recommends \
    snmp \
    libperl-dev \
    libsensors4-dev \
    collectd \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

COPY collectd.conf /etc/collectd/collectd.conf

VOLUME /var/lib/collectd/

CMD ["collectd", "-f"]
