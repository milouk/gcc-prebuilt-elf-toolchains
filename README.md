# Weekly builds are triggered every Sunday at 23:30.

## Prerequisites

`sudo apt-get install --yes git gcc g++ gperf bison flex texinfo help2man make libncurses5-dev autoconf automake libtool libtool-bin gawk wget bzip2 xz-utils unzip patch python3 libstdc++6 subversion`


## How to Build

* `sudo apt-get update && sudo apt-get upgrade`
* `cd Desktop`
* `git clone https://github.com/crosstool-ng/crosstool-ng`
* `cd crosstool-ng`
* `./bootstrap && ./configure`
* `make -j$(nproc --all)`
* `make install`
* `cd..`
* `mkdir build`
* `cd build`
* Copy the defconfig file into build Directory
* `ct-ng defconfig`
* `ct-ng build`

The Toolchain will be located in `/home/user/x-tools/`.
