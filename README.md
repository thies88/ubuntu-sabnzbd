# ubuntu-sabzbbd


### docker setup

```
docker create \
  --name=sabnzbd \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=Europe/London \
  -p 8080:8080 \
  -p 9090:9090 \
  -v /path/to/data:/config \
  -v /path/to/downloads:/downloads \
  -v /path/to/incomplete/downloads:/incomplete-downloads `#optional` \
  --restart unless-stopped \
  linuxserver/sabnzbd
  ```
