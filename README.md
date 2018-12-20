# docker-asterisk13-systemd
Asterisk 13 rpm running in centos 7 with systemd.
It runs /var on external volume an links /etc/asterisk to /var/lib/asterisk/astconfig to save custom configuration. Also you can put any custom module on /var/lib/asterisk/modplus (it is linked to /usr/lib64/asterisk/modules/modplus) and load it to asterisk. This image is builded with systemd. Enjoy it!


### Pull the image:

**docker pull etates/asterisk13-systemd:latest**


### Run the docker:

**docker run -d --name asterisk13 -v /sys/fs/cgroup:/sys/fs/cgroup:ro --tmpfs /run -v ast13vol:/var -v /etc/localtime:/etc/localtime:ro etates/asterisk13-systemd:latest**
