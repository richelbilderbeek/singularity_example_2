# singularity_example_2

Branch|[![Travis CI logo](pics/TravisCI.png)](https://travis-ci.org)
---|---
`master`|[![Build Status](https://travis-ci.org/richelbilderbeek/singularity_example_2.svg?branch=master)](https://travis-ci.org/richelbilderbeek/singularity_example_2)

Singularity example 2: lolcow on Cosmic

This example is similar to [example 1: lolcow](https://github.com/richelbilderbeek/singularity_example_1),
except that it uses a newer Ubuntu distribution, v18.10, also known
as Cosmic Cuttlefish.  

## Do not use 18.04

When changing the second line in `lolcow.def` to

```
From: ubuntu:18.04
```

You will get this error message:

```
richel@sonic:~/GitHubs/singularity_example_2$ ./build_container 
INFO:    Starting build...
INFO:    Running post scriptlet
+ apt-get -y update
Hit:1 http://us.archive.ubuntu.com/ubuntu bionic InRelease
Reading package lists... Done
+ apt-get -y install fortune cowsay lolcat
Reading package lists... Done
Building dependency tree... Done
E: Unable to locate package fortune
E: Unable to locate package cowsay
E: Unable to locate package lolcat
FATAL:   post proc: exit status 100
FATAL:   While performing build: while running engine: exit status 255
```