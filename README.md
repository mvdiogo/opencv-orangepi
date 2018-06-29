# Opencv on Orangepi and Ubuntu mate

Erase some software that is not need
```
sudo apt-get purge chromium-browser  
sudo apt-get purge wolfram-engine
sudo apt-get purge libreoffice*
sudo apt-get clean
sudo apt-get autoremove
```
use some software to remove more temp files
```
bleachbit
```
Create swap file if need
```
sudo fallocate -l 1G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
sudo swapon --show
free -m
```
to release swap
```
sudo swapoff
rm /swapfile
```
if you what to make permanent swap
```
sudo cp /etc/fstab /etc/fstab.bak
echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab
```
install some software
```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install build-essential git cmake pkg-config
sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
sudo apt-get install libxvidcore-dev libx264-dev
sudo apt-get install libgtk2.0-dev
sudo apt-get install libatlas-base-dev gfortran
```
download opencv-3.3.0-build-arm-ubuntu.tar.gz 
```
wget https://github.com/mvdiogo/opencv-orangepi/blob/master/opencv-3.3.0-build-arm-ubuntu.tar.gz
tar -xzvf opencv-3.3.0-build-arm-ubuntu.tar.gz
cd opencv-3.3.0-build-arm-ubuntu.tar.gz
make install
```
to install on python
```
sudo apt-get install python3-dev
wget https://bootstrap.pypa.io/get-pip.py
sudo python3 get-pip.py
pip3 install numpy
```
