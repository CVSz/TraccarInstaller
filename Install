#!/bin/bash

#
# Script to First time install traccar for Ubuntu 16.10 Yakkety installers requirements
# 

sudo apt-get -y update
sudo apt-get -y upgrade

echo "Install software requirement"
sudo apt-get -y install vim unp unrar unrar-free xdms p7zip p7zip-full unzip cabextract

sudo apt-get -y install apache2
sudo apache2ctl configtest

sudo apt-get -y install php libapache2-mod-php php-mcrypt php-mysql php-cli phpmyadmin apache2-utils
sudo apt-get -y install mysql-\* mysql-server libaio1 libevent-core-2.0-5 libjson-perl
sudo mysql_secure_installation

sudo apt-get -y install aptitude git curl wine wine-development innoextract makeself maven 
sudoapt-get -y install ruby python-software-properties software-properties-common python-xattr

sudo add-apt-repository ppa:webupd8team/java
sudo apt-get -y update
sudo apt-get -y install default-jre default-jdk openjdk-8-jdk oracle-java8-set-default java gcj-4.6-jre-headless openjdk-\*
sleep 5

echo "Download Source Code of Traccar"
git clone https://github.com/tananaev/traccar.git
cd traccar
git clone https://github.com/tananaev/traccar-web.git
sleep 5

echo "Missing ext-6.2.0 (https://www.sencha.com/legal/GPL/)"
wget http://cdn.sencha.com/cmd/6.2.0/no-jre/SenchaCmd-6.2.0-linux-amd64.sh.zip
unzip SenchaCmd-6.2.0-linux-amd64.sh.zip
./SenchaCmd-6.2.0.103-linux-amd64.sh
sleep 5

echo "Missing sencha cmd package (https://www.sencha.com/products/extjs/cmd-download/)"
wget http://cdn.sencha.com/ext/gpl/ext-6.2.0-gpl.zip
unzip -o ext-6.2.0-gpl.zip -d ../../
sleep 5

echo "Missing yajsw-*.zip (https://sourceforge.net/projects/yajsw/files/)"
wget https://sourceforge.net/projects/yajsw/files/latest/download
mv download traccar/setup/yajsw-beta-12.07.zip
sleep 5

echo "ls innosetup-*.exe" "Missing isetup-*.exe (http://www.jrsoftware.org/isdl.php)"
wget http://www.jrsoftware.org/download.php/is.exe
mv is.exe traccar/setup/innosetup-5.5.9.exe
sleep 5
