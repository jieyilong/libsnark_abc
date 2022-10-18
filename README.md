# libsnark ABC

Minimal examples to use libsnark.

## Reference

- https://github.com/christianlundkvist/libsnark-tutorial
- https://github.com/howardwu/libsnark-tutorial

## Compilation

Please following the steps here: https://zhuanlan.zhihu.com/p/100809637


If `git submodule update --init --recursive` errors out, please follow instructions [here](https://github.com/jieyilong/libsnark#build-instructions) to download and compile libsnark. 

Next, execute the following commands, where `<PATH/TO/LIBSNARK>` points to the downloaded libsnark lib above:

```shell
git clone https://github.com/jieyilong/libsnark_abc
cd libsnark_abc
rm -rf depends/libsnark
cp -r <PATH/TO/LIBSNARK> depends/
mkdir build && cd build && CPPFLAGS=-I/usr/local/opt/openssl/include LDFLAGS=-L/usr/local/opt/openssl/lib PKG_CONFIG_PATH=/usr/local/opt/openssl/lib/pkgconfig cmake -DWITH_PROCPS=OFF -DWITH_SUPERCOP=OFF ..

make
```
