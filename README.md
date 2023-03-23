# OpenSSL for RACE

This repo provides scripts to custom-build the
[OpenSSL library](https://openssl.org) for RACE.

## License

The OpenSSL library is licensed under Apache 2.0.

Additionally the build scripts in this repo are licensed under Apache 2.0.

## Dependencies

OpenSSL has no dependencies on any custom-built libraries.

## How To Build

The [ext-builder](https://github.com/tst-race/ext-builder) image is used to
build OpenSSL.

```
git clone https://github.com/tst-race/ext-builder.git
git clone https://github.com/tst-race/ext-openssl.git
./ext-builder/build.py \
    --target linux-x86_64 \
    ./ext-openssl
```

## Platforms

OpenSSL is built for the following platforms:

* `android-x86_64`
* `android-arm64-v8a`

It is also used on Linux but can be installed via `apt`.

## How It Is Used

OpenSSL is used directly by the RACE core. It is also a dependency for other
libraries.
