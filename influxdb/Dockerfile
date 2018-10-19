FROM resin/raspberrypi3-debian:stretch

RUN apt-get update && apt-get install -yq \
  fontconfig-config fonts-dejavu-core libfontconfig1 ucf \
  wget && \
  apt-get clean && rm -rf /var/lib/apt/lists/*

RUN wget -O /tmp/influxdb.deb https://dl.influxdata.com/influxdb/releases/influxdb_1.6.3_armhf.deb && \
    dpkg -i /tmp/influxdb.deb && rm /tmp/influxdb.deb

RUN sed -i 's|/var/lib/influxdb|/data/influxdb|g' /etc/influxdb/influxdb.conf

CMD ["/usr/bin/influxd"]
