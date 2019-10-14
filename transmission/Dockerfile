FROM debian:10.1
RUN apt-get -y update \
  && apt-get -y install curl dnsutils jq openvpn transmission-daemon unzip vim

RUN mkdir -p /openvpn

COPY ./atlanta.ovpn /openvpn
COPY ./pia-login.conf /openvpn
COPY ./settings.json /var/lib/transmission-daemon/info/settings.json
COPY ./start-transmission /openvpn

RUN chmod 775 /var/lib/transmission-daemon/info/settings.json
RUN curl -o /openvpn/openvpn.zip https://www.privateinternetaccess.com/openvpn/openvpn.zip
RUN unzip /openvpn/openvpn.zip -d /openvpn

WORKDIR /transmission

CMD [ "/openvpn/start-transmission" ]
