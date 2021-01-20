## method 1

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

delete the dir:proxychains-ng/   &    /usr/local/proxychains   


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

remove the proxychains  &   delete proxychains.conf.dpkg-dist   & delete proxychains.conf


## method2

```
export ALL_PROXY=socks5://127.0.0.1:1080
```
failed
```
unset ALL_PROXY
```


## method3


```
sudo apt install proxychains(不小心在/etc目录下使用了该命令)
```
提示找不到 Can't locate proxychains.conf: No such file or directory

create & delete proxychain.conf


## method4
again  use the   https://github.com/rofl0r/proxychains-ng.git

but doesn't work
