# WSSH

# Introduction

## 1. WSSH

WSSH stands for Web-based SSH, which intends to access SSH servers through standard web browsers.

## 2. gevent-websocket

gevent-websocket is a WebSocket library for the gevent networking library.

## 3. paramiko 
paramiko is a module for python 2.2 (or higher) that implements the SSH2 protocol for secure connections to remote machines.

# Installation

## 1. Install Python Tool 

```

apt-get install python-pip

apt-get install python-dev

```

For thoses who need to use proxy servers:

```

export http_proxy=http://******

export https_proxy=http://******

```

## 2. Download wssh package

```

git clone https://github.com/aluzzardi/wssh.git

cd wssh/

```
## 3. Setup WSSH

Install the packages needed by wssh:

```
pip install -r requirements_server.txt

pip install -r requirements.txt

```

wssh setup:

```
python setup.py install

```

## 4. Usage

Run wssh server:

```
wsshd

```
Connect through web interface:

```
URL: http://ip address of your remote machine:5000

```
web connect interface:

![alt text](https://raw.githubusercontent.com/Sherry22/html5-vdi/master/wssh/screenshot/connect%20to%20remote%20SSH%20server.png)
console:

![alt text](https://raw.githubusercontent.com/Sherry22/html5-vdi/master/wssh/screenshot/console.png)









