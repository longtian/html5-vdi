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

'''
<b>
apt-get install python-pip

apt-get install python-dev
</b>
'''

For thoses who need to use proxy servers:

'''
export http_proxy=http://******
export https_proxy=http://******
'''
## 2. Download wssh package

'''
<b>
git clone https://github.com/aluzzardi/wssh.git
cd wssh/
</b>
'''
## 3. Setup WSSH

Install the package needed by wssh:
'''
<b>
pip install -r requirements_server.txt
pip install -r requirements.txt
</b>
'''
wssh setup:

'''
<b>
python setup.py install
</b>
'''
## 4. Usage

Run wssh server:
'''
<b>
wsshd
</b>
'''
Connect through web interface:
'''
<b>
URL: http://*ip address of your remote machine*:5000
</b>
'''










