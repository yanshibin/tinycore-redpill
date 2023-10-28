<a href="https://github.com/pocopico/tinycore-redpill/releases"><img src="https://img.shields.io/github/release/pocopico/tinycore-redpill.svg"></a>
<a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fpocopico%2Ftinycore-redpill&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false"/></a>
[![](https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86)](https://github.com/sponsors/pocopico)


# tinycore-redpill

This is a testing version. Do not use unless you are certain you have no data to lose.

Please note that minimum recommended memory size for configuring the loader is 2GB

# Instructions 

A normal build process would start with :

### 1. Image burn

* a. For physical gunzip and burn img file to usb stick

* b. For virtual gunzip and use the provided vmdk file 

### 2. Boot tinycore

### 3. ssh to your booted loader or just open the desktop terminal 

### 4. Bring over your json files (`global_config.json`, `custom_config.json`, `user_config.json`)

### 5. Check the contents of user_config.json, if satisfied keep or else run:

* a. Perform a rploader update by running `./rploader.sh update`

* b. Perform a fullupdate to update all local files of your image by running `./rploader.sh fullupgrade`

* c. Change you serial and mac address by running `./rploader.sh serialgen DS3615xs`, if you want to use WoL you can use realmac option here e.g. `./rploader.sh serialgen DS3515xs realmac`

* d. Update user_config.json with your VID:PID of your usb stick by running `./rploader.sh identifyusb`

* e. Update user_config.json with your SataPortMap and DiskIdxMap by running `./rploader.sh satamap`

* f. Backup your changes to local loader disk by running `./rploader.sh backup`

### 6. `./rploader.sh build ds3615xs-7.0.1-42218`
