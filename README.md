## Fixed vhost for iframe in OpenLiteSpeed
```
cd ~
if [ -f /usr/local/lsws/bin/lswsctrl ]; then
mkdir -p /usr/local/directadmin/data/templates/custom
cd /usr/local/directadmin/data/templates/custom
wget --no-check-certificate -q "https://raw.githubusercontent.com/shizhaoa8/vn/main/openlitespeed_vhost.conf.CUSTOM.3.txt" -O openlitespeed_vhost.conf.CUSTOM.3.pre
cd ~
cd /usr/local/directadmin/custombuild
./build rewrite_confs
cd ~
/usr/local/lsws/bin/lswsctrl restart
fi
```
