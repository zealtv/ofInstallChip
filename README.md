# Script and instruction for building openFrameworks on C.H.I.P.
Tested with openFrameworks 0.9.8 and CHIP OS 4.4.13 (GUI and PocketCHIP versions)  -  note it seems this doesn't work on the headless version of the CHIP OS due to some missing EGL related package.  Some research required to figure out what's going on there - if you know please let me know.

From a freshly flashed chip:

update and upgrade

`sudo apt-get update`

`sudo apt-get upgrade`


install git, clone this repo and cd into repo directory

`sudo apt-get install git`

`git clone https://github.com/zealtv/ofInstallChip.git`

`cd ofInstallChip`


make excecutable and run the install_dependencies_chip.sh script in this repo - this is the same as the standard install_dependencies script with mesa related packages removed.

`chmod +x ./install_dependencies_chip.sh`

`sudo ./install_dependencies_chip.sh`


download and extract openFrameworks for linux arm7:

`cd where/ever/you/want/to/install/of`

`wget http://openframeworks.cc/versions/v0.9.8/of_v0.9.8_linuxarmv7l_release.tar.gz`

`tar -xf of_v0.9.8_linuxarmv7l_release.tar.gz`


go to script folder, install codecs and build openFrameworks 

`cd of_v0.9.8_linuxarmv7l_release/scripts`

`sudo linux/debian/install_codecs.sh`

`linux/compileOF.sh`


rebuild poco 

`cd ../scripts/apothecary`

`./apothecary -tlinuxarmv7l update poco`


Done! Go build an example and test
