sudo su

rpi-rw

cd /tmp

git clone https://github.com/pyserial/pyserial.git

cd pyserial

python setup.py install

pistar-watchdog.service stop

systemctl stop mmdvmhost.timer

systemctl stop mmdvmhost.service

cd ~/MHI-TJC

python nextion.py TJC3224T024-.tft /dev/ttyUSB0
