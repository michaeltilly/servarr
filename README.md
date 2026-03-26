## Need to setup .env for servarr stack

### .env file should look like this if using nordvpn

```
# General UID/GIU and Timezone
TZ=timezone
PUID=1000
PGID=1000

VPN_SERVICE_PROVIDER=nordvpn
VPN_TYPE=openvpn # or wireguard
OPENVPN_USER=
OPENVPN_PASSWORD=
SERVER_COUNTRIES=
SERVER_CATEGORIES=P2P

# Heath check duration
HEALTH_VPN_DURATION_INITIAL=120s
```

## Run this command to test gluetun health
```
docker run --rm --network=container:gluetun alpine:3.18 sh -c "apk add wget && wget -qO- https://ipinfo.io"
```
