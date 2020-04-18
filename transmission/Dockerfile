FROM debian:10.1
RUN apt-get -y update \
  && apt-get -y install curl dnsutils jq openvpn transmission-daemon unzip vim

RUN mkdir -p /openvpn

COPY ./expressvpn_dallas2.ovpn /openvpn
COPY ./expressvpn-login.conf /openvpn
COPY ./settings.json /var/lib/transmission-daemon/info/settings.json
COPY ./start-transmission /openvpn

RUN chmod 775 /var/lib/transmission-daemon/info/settings.json

WORKDIR /transmission

CMD [ "/openvpn/start-transmission" ]
