# IP RANDOM


## INDEX

- [IP RANDOM](#ip-random)
  - [INDEX](#index)
  - [BADGES](#badges)
  - [FIRST UPDATE](#first-update)
  - [INTRODUCTION](#introduction)
  - [PREREQUISITES](#prerequisites)
  - [INSTALL](#install)
  - [CONFIG](#config)
  - [LICENSE](#license)


## BADGES

[![pipeline status](https://gitlab.com/oda-alexandre/ip_random/badges/master/pipeline.svg)](https://gitlab.com/oda-alexandre/ip_random/commits/master)


## FIRST UPDATE

Date: 01-01-01


## INTRODUCTION

This repository contains a script that allows of change ip at boot.


## PREREQUISITES

Use [OpenVpn](https://openvpn.net)


## INSTALL

```apt-get update```

```apt-get install --no-install-recommends openvpn```

```systemctl restart openvpn```

```systemctl enable openvpn```

```git clone https://gitlab.com/oda-alexandre/ip_random.git ~/ip_random```

```mv -f ~/ip_random/ip-random /etc/init.d/```

```chmod +x /etc/init.d/ip-random```

```update-rc.d -f ip-random defaults```

```rm -rf ~/ip_random```

```mkdir /usr/share/openvpn/vpn```


## CONFIG

1 - Most of the VPN providers have the configurations available for OpenVPN. Check if your VPN provider supports OpenVPN and look for their files of configuration openvpn.conf.

2 - put the files openvpn.conf in the folder / usr / share / openvpn / vpn by creating a folder by files openvpn.conf.

3 - Add this line for auto autentification in the openvpn.conf files.

```auth-user-pass auth.txt```

4 - Add an auth.txt file next to your openvpn.conf files with your username & password.

```username```

```password```


## LICENSE

[![GPLv3+](http://gplv3.fsf.org/gplv3-127x51.png)](https://gitlab.com/oda-alexandre/ip_random/blob/master/LICENSE)
