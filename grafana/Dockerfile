FROM resin/raspberrypi3-debian:stretch

RUN apt-get update && apt-get install -yq \
  fontconfig-config fonts-dejavu-core libfontconfig1 ucf \
  wget && \
  apt-get clean && rm -rf /var/lib/apt/lists/*

RUN wget -O /tmp/grafana.deb https://s3-us-west-2.amazonaws.com/grafana-releases/release/grafana_5.3.1_armhf.deb && \
    dpkg -i /tmp/grafana.deb && rm /tmp/grafana.deb

COPY ./grafana.ini /usr/share/grafana/conf/custom.ini
COPY ./grafana.db /data/grafana/grafana.db

CMD ["/usr/sbin/grafana-server", "-homepath", "/usr/share/grafana"]
