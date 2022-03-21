# Tools

### Bettercap

{% embed url="https://github.com/bettercap/bettercap" %}

{% embed url="https://github.com/koutto/pi-pwnbox-rogueap/wiki" %}



## Wifite

This is a [Python script](https://github.com/derv82/wifite2) for automated auditing of wireless networks.

{% hint style="danger" %}
Uninstalling is not easy. It is recommended to run in a separate environment.
{% endhint %}

```
# Run wifite
git clone https://github.com/derv82/wifite2.git
cd wifite2
sudo ./Wifite.py

# Install Wifite
sudo python setup.py install
```

This script can be run in the WiFi Pineapple (Tetra is recommended) based in [this guide](https://forums.hak5.org/topic/42244-wifite2-wifi-pineapple-setup/).

```
opkg update

# tetra
opkg install git git-http coreutils-stty

git clone git://github.com/derv82/wifite2.git

cd wifite2/

./Wifite.py
```

