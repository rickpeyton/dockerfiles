# Transmission Docker Setup with Private Internet Access (PIA)

## Modify a ExpressVPN ovpn file

I made a copy of the Dallas 2 ovpn file and named it expressvpn_dallas2.ovpn

In expressvpn_dallas2.ovpn =>

`auth-user-pass` to `auth-user-pass /openvpn/expressvpn-login.conf`

## Create a expressvpn-login.conf

Line 1 is your ExpressVPN username
Line 2 is your ExpressVPN password

## Verify that you are connected

Something like

`docker exec -it transmission_transmission_1 curl ifconfig.co/json | jq`

And get something like

```json
{
  "ip": "45.56.151.68",
  "ip_decimal": 758683460,
  "country": "United States",
  "country_eu": false,
  "country_iso": "US",
  "city": "Dallas",
  "latitude": 32.7787,
  "longitude": -96.8217,
  "asn": "AS36351",
  "asn_org": "SOFTLAYER",
  "user_agent": {
    "product": "curl",
    "version": "7.64.0",
    "raw_value": "curl/7.64.0"
  }
}
```