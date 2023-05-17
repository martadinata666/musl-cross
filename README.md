# musl gcc cross build
* https://musl.cc
* https://git.zv.io/toolchains/musl-cross-make

Due https://musl.cc not updating binaries over 2 years, but upstream git updating, rebuild musl-cross-make ourself, depends on upstream [hashes](https://git.zv.io/toolchains/musl-cross-make/-/tree/master/hashes)

## Local build
* Clone upstream git 
```
$ git clone --depth=1 https://git.zv.io/toolchains/musl-cross-make musl-cross
```
* Copy config.mak.yourmodification to `musl-cross/config.mak`, [config.mak reference](https://git.zv.io/toolchains/musl-cross-make/-/blob/master/config.mak.dist)
* `cd musl-cross`
* `make -j$(nproc)
* `make install`
* The compiled binary at `output` path

The output path already portable copy to another system or bind mount to another container, etc.
