# Muduo Tutorial



## Install on Debian or Ubuntu

### Prerequisites
```shell
# Required
$ sudo apt-get install g++ libboost-dev cmake

# Optional libraries

# more boost libraries
$ sudo apt-get install libboost-test-dev libboost-program-options-dev

# Protobuf and tcmalloc from Google
$ sudo apt-get install libgoogle-perftools-dev protobuf-compiler libprotobuf-dev

# some C libraries
$ sudo apt-get install zlib1g-dev libc-ares-dev libcurl4-openssl-dev

# GD2
$ sudo apt-get install libgd-dev  # or libgd2-noxpm-dev
```

### Get source code and compile
```shell
$ git clone https://github.com/chenshuo/muduo.git
$ cd muduo
$ ./build.sh
# check output files in ../build/release/bin

# Build debug version
$ BUILD_TYPE=debug ./build.sh
```

If you want to run binary on a different machine, comment out `-march=native` in `CMakeLists.txt`.  Otherwise you may see `SIGILL` if the CPU of target machine is older than compile machine.

## Supported Linux Distros

|Tier|Linux | Kernel |GCC|Boost|
|------|--------|
|3|Debian 6| 2.6.32| 4.4.5|1.42.0|
|1|Debian 7| 3.2.0 | 4.7.2|1.49.0|
|2|Debian 8| 3.16.0| 4.9.2|1.55.0|
|3|Ubuntu 10.04| 2.6.32 | 4.4.3 | 1.40.0 |
|2|Ubuntu 12.04| 3.2.0  | 4.6.3 | 1.46.1 |
|1|Ubuntu 14.04| 3.13.0 | 4.8.2 | 1.54.0 |
|2|Ubuntu 16.04| 4.4.0 | 5.3.1 | 1.58.0 |
All are 64-bit distros.
