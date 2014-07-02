- qemu is used as virtualization backend
- git to grab
-- spice-html5
-- websockify
- nginx will hold static files

`
apt-get install qemu
apt-get install git
apt-get install nginx

cd /usr/share/nginx/html/

git clone git://anongit.freedesktop.org/spice/spice-html5
git clone https://github.com/kanaka/websockify.git

wget http://wiki.qemu.org/download/linux-0.2.img.bz2
bzip2 -d linux-0.2.img.bz2

qemu linux-0.2.img -spice port=5950,password=12345678
websockify/websockify.py 5959 localhost:5950

http://localhost/spice-html5/spice_auto.html?host=localhost&password=12345678&port=5959
`
