# rtl8188eus
Wifi driver support for rtl8188eu, rtl8188eus and rtl8188etv chips and working under the new kernel for Linux (4.14.x).
More information about your wifi device can be found here: https://wikidevi.com.

Compiling & Building
---------
### Dependencies
To compile the driver, you need to have make and a compiler installed. In addition,
you must have the kernel headers installed. If you do not understand what this means,
consult your distro. if compile a new kernel, you will need to set two parameters
with make: KSRC=path_to_kernel_source and KVER=kernel_version. 
### Compiling

> make all

### Installing

> sudo make install
