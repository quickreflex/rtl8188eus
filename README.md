# rtl8188eus
Wifi driver support for rtl8188eu, rtl8188eus and rtl8188etv chips and working under the new linux kernel (5.1.x).
More information about your wifi device can be found here: https://wikidevi.com.

Compiling & Building
---------
### Dependencies
To compile the driver, you need to have make and a compiler installed. In addition,
you must have the kernel headers installed. If you do not understand what this means,
consult your distro. if compile a new kernel, you will need to set two parameters
with make: KSRC=path_to_kernel_source and KVER=kernel_version. The same goes for installation.

### Download
```
git clone -b v5.2.2.4 https://github.com/quickreflex/rtl8188eus.git
cd rtl8188eu
```

### Compiling & Installing
```
make all
make install
```

Or with DKMS
```
dkms add .
dkms build 8188eu/1.0
dkms install 8188eu/1.0
```

Switch modes
---------
### Supported interface modes
```
* IBSS
* managed
* AP
* monitor
* P2P-client
* P2P-GO
```
### For setting interface modes
```
ifconfig wlan0 down
iw dev wlan0 set type managed
ifconfig wlan0 up
```
### For setting TX power
```
iw wlan0 set txpower fixed 1300
```
