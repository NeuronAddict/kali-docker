# Docker for build kali kernel

## get sources

```
kali-docker$ cd src
$ git clone <your kernel>
```

## config

Change env vars in docker-compose or when you launch container :

MAKE_CONFIG=lineageos_bullhead_defconfig # default config passed to make
SRC_SUBDIR=lineage-15.0 # subdir in src where are your kernel sources

## build container

```
$ git clone https://github.com/NeuronAddict/kali-docker.git
$ cd kali-docker
$ docker-compose build
```

## run into env

```
$ docker-compose run nethunter-kernel-build
```

# example

```
kali-docker/src$ git clone https://github.com/LineageOS/android_kernel_lge_bullhead.git --single-branch -b lineage-15.0
$ cd ..
$ nano docker-compose
# in enviroment section : 
# MAKE_CONFIG=lineageos_bullhead_defconfig # default config passed to make
# SRC_SUBDIR=lineage-15.0 # subdir in src where are your kernel sources
$ docker-compose build
$ docker-compose run nethunter-kernel-build
```