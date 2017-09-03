Fireduck os
====================================================================



Host System Preparation :
====================================================================
You need a install various packages.

exsample: Ubuntu14.04  
sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib \  
build-essential chrpath socat libsdl1.2-dev xterm make xsltproc docbook-utils \  
fop dblatex xmlto autoconf automake libtool libglib2.0-dev



Build Fireduck OS :
====================================================================
cd /path/to/work

repo init -u https://github.com/TokaidoLUG/fireduckos

repo sync

source meta-fireduck/scripts/fireducksetup.sh -m intel-mobile-64 enlightenment   
or  
source meta-fireduck/scripts/fireducksetup.sh -m jetson-tk1 enlightenment   


bitbake fireduck-image


Select machine :
====================================================================
The fireduck OS has the following machine:

intel-mobile-64 : intel 64bit (include UEFI32 boot support)  
intel-64 : intel 64bit (exclude UEFI32 boot support)  
jetson-tk1 : NVIDIA jetson TK1 board  



Add additional functions :
====================================================================
The fireduck OS has the following additional components:

enlightenment : enlightenment desktop  
browser : web browser  

fireduckwm : fireduck desktop (experimental)  

Activate additional functions using the setup script.

source meta-fireduck/scripts/fireducksetup.sh -m *machine* *functions*

For example :  
source meta-fireduck/scripts/fireducksetup.sh -m jetson-tk1 enlightenment browser  

