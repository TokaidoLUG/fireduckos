# Fireduck OS

## Host System Preparation

You need a install various packages.

example: Ubuntu 14.04 and 16.04  

```
sudo apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib \  
build-essential chrpath socat libsdl1.2-dev xterm make xsltproc docbook-utils \  
fop dblatex xmlto autoconf automake libtool libglib2.0-dev
```

## Build Fireduck OS

```
cd /path/to/work
```

```
repo init -u https://github.com/TokaidoLUG/fireduckos
```

```
repo sync
```

```
source meta-fireduck/scripts/fireducksetup.sh -m intel-mobile-64 enlightenment   
```

or  

```
source meta-fireduck/scripts/fireducksetup.sh -m jetson-tk1 enlightenment   
```

```
bitbake fireduck-image
```

### Select machine

The Fireduck OS has the following machine:

- `intel-mobile-64` : intel 64bit (include UEFI32 boot support)  
- `intel-64` : intel 64bit (exclude UEFI32 boot support)  
- `jetson-tk1` : NVIDIA jetson TK1 board  

### Add additional functions

The Fireduck OS has the following additional components:

- `plasma` : kde plasma desktop (experimental)  
- `lxqt` : lxqt desktop (experimental)  
- `browser` : web browser  
- `fireduckwm` : fireduck desktop (may discontinued)  
- `enlightenment` : enlightenment desktop (may discontinued)  

Activate additional functions using the setup script.

```
source meta-fireduck/scripts/fireducksetup.sh -m <machine> <functions>
```

For example :  

```
source meta-fireduck/scripts/fireducksetup.sh -m jetson-tk1 enlightenment browser  
```
