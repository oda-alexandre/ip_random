# IP RANDOM


## INDEX

- [Introduction](#INTRODUCTION)
- [Prerequis](#PREREQUIS)
- [Installation](#INSTALLATION)
- [CONFIGURATION](#CONFIGURATION)
- [License](#LICENSE)


## INTRODUCTION

Ce repository contient un script qui permet de changer d'ip à chaque démarrage en sélectionnant aléatoirement un fichier openvpn.conf.


## PREREQUIS

Installer [OpenVpn](https://openvpn.net)


## INSTALLATION

```
apt update
apt install --no-install-recommends openvpn
systemctl restart openvpn
systemctl enable openvpn
git clone https://github.com/oda-alexandre/ip_random.git ~/ip_random
mv -f ~/ip_random/ip-random /etc/init.d/
chmod +x /etc/init.d/ip-random
update-rc.d -f ip-random defaults
rm -rf ~/ip_random
mkdir /usr/share/openvpn/vpn
```


## CONFIGURATION

1 - La plupart des fournisseurs de VPN ont des configurations disponibles pour OpenVPN. Vérifiez si votre fournisseur VPN prend en charge OpenVPN et recherchez leurs fichiers de configuration openvpn.conf.

2 - Placez les fichiers openvpn.conf dans le dossier /usr/share/openvpn/vpn en créant un dossier par fichiers openvpn.conf.

3 - Ajoutez cette ligne pour l'autentification automatique dans les fichiers openvpn.conf.

```
auth-user-pass auth.txt
```

4 - Ajoutez un fichier auth.txt a cote de vos fichiers openvpn.conf avec votre username & password.

```
username
password
```

## LICENSE

[![GPLv3+](http://gplv3.fsf.org/gplv3-127x51.png)](https://github.com/oda-alexandre/ip_random/blob/master/LICENSE)
