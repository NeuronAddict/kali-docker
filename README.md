# Docker for build kali kernel

## build container

```
$ git clone https://github.com/NeuronAddict/kali-docker.git
$ cd kali-docker
$ docker-compose build
```

## get sources

```
kali-docker$ cd src
$ git clone <your kernel>
```

## run into env

```
$ docker-compose run kali-kernel-build
/src# make help # RTFM !
/src# make menuconfig
...
```