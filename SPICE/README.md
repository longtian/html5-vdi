
SPICE
===================================

# Introduction
## 1. QEMU 
A virtualization hosting applciation.

## 2. spice-html5
Partial implementation of SPICE protocol use websocket.
## 3. websockify
Python script to convert almost any protocol into websocket.

## 4. nginx
Web server to serve html/ css/ javascript files.

# Installation
Install qemu, git and nginx server

```
apt-get install qemu, git, nginx
```
Clone spice-html5 and websocketfy repos

```
cd /usr/share/nginx/html/
git clone git://anongit.freedesktop.org/spice/spice-html5
git clone https://github.com/kanaka/websockify.git
```
Download a 8MB Linux for testing

```
wget http://wiki.qemu.org/download/linux-0.2.img.bz2
bzip2 -d linux-0.2.img.bz2
```
# Running 

Start a virtual machine instance with SPICE turned on

```
qemu linux-0.2.img -spice port=5950,password=12345678 &
```

Use websockify to redirect the spice protocol for websocket access

```
websockify/websockify.py 5959 localhost:5950 &
```

# Visit the link

```
http://localhost/spice-html5/spice_auto.html?host=localhost&password=12345678&port=5959
```
