# cypress-from-dev-container

Trying to get Cypress running from within an Ubuntu docker container on macOS and Windows.

So far, XQuartz is working on macOS.

First Start XQuartz and in **Applications > Terminal** run `xhost + $LOCAL_IP`, replacing `$LOCAL_IP` with your actual local IP address.

```shell
docker run --rm -it --env="DISPLAY=$(ifconfig | grep "inet " | grep -Fv 127.0.0.1 | awk '{print $2}'):0" -v /tmp/.X11-unix:/tmp/.X11-unix:rw cy-dev /bin/bash
```
