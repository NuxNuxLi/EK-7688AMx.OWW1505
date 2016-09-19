# How to compile?
## 1.install depend
$ sudo apt-get update

$ sudo apt-get install git g++ make libncurses5-dev subversion libssl-dev gawk libxml-parser-perl unzip wget python \
xz-utils vim
## 2.download the source use git
$ git clone https://github.com/NuxNuxLi/EK-7688AMx.OWW1505.git
## 3.update the feeds
$ cd EK-7688AMx.OWW1505
$ ./scripts/feeds update -a

$ ./scripts/feeds install -a
## 4.config
$ make menuconfig
select the target:

Target System(Ralink RT288x/RT3xxx) --->

Subtarget(MT7688 based board) --->

Target Profile(LinkIt7688) --->

## 5.make
$ make -j4
## 6.image
the binary image name like this in bin/ramips/:
openwrt-ramips-mt7688-LinkIt7688-squashfs-sysupgrade.bin

# How to start AirKiss?

0. Download [AirKissDebugger.apk](http://iot.weixin.qq.com/wiki/doc/wifi/AirKissDebugger.apk)
0. Start AirKiss process -- `aac`
0. Run AirKissDebugger.apk and input SSID and PASSWORD
