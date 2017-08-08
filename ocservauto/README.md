## Ocservauto For Debian/Ubuntu

This script may help you setup your own openconnect_server in debian(>=7),ubuntu(=14.04).

这是一枚适用于deibian的openconnect_server安装脚本。中文详情 [戳这里](http://www.fanyueciyuan.info/fq/ocserv-debian.html)

============

## USAGE
```shell
apt-get update
apt-get upgrade
apt-get install wget
wget https://raw.githubusercontent.com/ddzzhen/eazy-for-ss/ocserv11/ocservauto/ocservauto.sh --no-check-certificate -O ocservauto.sh
bash ocservauto.sh
```

>some documents come from origin,will change future.

Profiles in /etc/ocserv/

When you change the profiles,restart the vpn server.
```shell
/etc/init.d/ocserv restart
```
stop the vpn server.
```
/etc/init.d/ocserv stop
```
debug mode.(logs)
```
/etc/init.d/ocserv debug
```
You can get help 
```shell
bash ocservauto.sh h
```
---
useradd.
```
sudo ocpasswd -c /etc/ocserv/ocpasswd username
```
certificate login.
```
add:
bash ocservauto.sh gc
delet:
bash ocservauto.sh rc
```
others.
```
upgrade:
bash ocservauto.sh ug
force reinstall:
bash ocservauto.sh ri
open the user and certificate login:
bash ocservauto.sh pc
>Tip: One method can use at least.
anyconnect:
untrusted certificates is allowed.
>Tip:window mobile must insert "https://"+example.com:port
bertter to use(depend environment):
>connected but no data:smaller the "dpd","mobile-dpd"
>high ping:make "output-buffer" to 10
>Tip:small "output-buffer" will influence the mount of data.
#no-route
no-route = 192.168.0.0/255.255.0.0
no-route = 172.16.0.0/255.240.0.0
no-route = 169.254.0.0/255.255.0.0
no-route = 127.0.0.0/255.0.0.0

============

## LICENCE
Ocservauto For Debian Copyright (C) liyangyijie released under GNU GPLv2

Ocservauto For Debian Is Based On SSLVPNauto v0.1-A1

SSLVPNauto For Debian Copyright (C) Alex Fang frjalex@gmail.com released under GNU GPLv2



    Copyright (C) 2015  liyangyijie

    This program is free software; you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation; either version 2 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.
