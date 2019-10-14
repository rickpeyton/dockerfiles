# Transmission Docker Setup with Private Internet Access (PIA)

## Modify a PIA ovpn file

I made a copy of the US\ Atlana.ovpn file and named it atlanta.ovpn

`auth-user-pass` to `auth-user-pass /openvpn/pia-login.conf`

## Create a pia-login.conf

Line 1 is your PIA username
Line 2 is your PIA password
