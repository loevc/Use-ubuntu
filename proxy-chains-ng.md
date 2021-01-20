```
git clone https://github.com/rofl0r/proxychains-ng.git
cd proxychains-ng/
./configure --prefix=/usr/local/proxychains --sysconfdir=/etc
make -j
sudo make install
sudo make install-config
```

alter /etc/proxychains.conf   last column 
**socks4 127.0.0.1 9095**  to
**socks5 127.0.0.1 1080**

1080 is shadowsocks 's  local port.

use method

```
proxychains4 curl google.com
```
found is not had proxychains

use 
```
sudo apt install proxychains
```

still failed



