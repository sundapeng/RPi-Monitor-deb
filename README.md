# [**RPi-Monitor-deb**](http://rpi-experiences.blogspot.fr/)

**RPi-Monitor-deb** is the project packaging [**RPi-Monitor**](https://github.com/XavierBerger/RPi-Monitor) into a debian package. **RPi-Monitor** is a self monitoring application designed to run on [Raspberry Pi](http://www.raspberrypi.org/).

Installation, usage and customization are detailed into the official web site: [http://rpi-experiences.blogspot.fr/](http://rpi-experiences.blogspot.fr/)


## Prerequisite

Before using **RPi-Monitor-deb** it is required to install the dependencies. To do so, execute the following command:

    sudo apt-get install dpkg-dev 

## Package creation

Clone RPi-Monitor and RPi-Minitor-dev:

    git clone https://github.com/XavierBerger/RPi-Monitor.git
    git clone https://github.com/XavierBerger/RPi-Monitor-deb.git

Build package:

    cd RPi-Monitor-deb
    ./build-deb.sh
   
## Install

    wget -O rpimonitor_2.10-1_all.deb https://github.com/XavierBerger/RPi-Monitor-deb/blob/master/repo/rpimonitor_2.10-1_all.deb?raw=true
    sudo dpkg -i rpimonitor_2.10-1_all.deb
    sudo apt-get -f install

~~## Repository~~

~~Build script also create a debian repository. To use this repository follow the instruction bellow:~~

~~Activate https transport for apt:~~

~~sudo apt-get install apt-transport-https ca-certificates~~

~~Add my public key to the trusted key list for apt:~~

~~sudo apt-key adv --recv-keys --keyserver keyserver.ubuntu.com 2C0D3C0F~~

~~Execute the following command to add rpimonitor into your list of repository:~~

~~sudo wget http://goo.gl/rsel0F -O /etc/apt/sources.list.d/rpimonitor.list~~

~~This will add the file `/etc/apt/source.list.d/rpimonitor.list` containing:~~

~~# RPi-Monitor official repository~~
~~deb https://github.com XavierBerger/RPi-Monitor-deb/raw/master/repo/~~

~~**Note**: To test unstable version, replace *master* by *devel* into the upper line.~~

~~Install **RPi-Monitor**~~

~~sudo apt-get update~~
~~sudo apt-get install rpimonitor~~

~~For update (when a new release of RPi-Monitor is available)~~

~~sudo apt-get update~~
~~sudo apt-get upgrade~~


## Authors

**Xavier Berger**

+ [http://rpi-experiences.blogspot.fr](http://rpi-experiences.blogspot.fr)
