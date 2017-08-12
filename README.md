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

source meta-fireduck/scripts/fireducksetup.sh -m intel-mobile-64  
or  
source meta-fireduck/scripts/fireducksetup.sh -m jetson-tk1  


bitbake fireduck-image

