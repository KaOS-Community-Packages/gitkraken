# gitkraken

Git client with efficiency, elegance and reliability at the core

[Homepage](https://www.gitkraken.com/)

### Required package from KCP:
```
kcp -di curl-kcp
```

### Required manual build:
The needed dependency `libcurl-gnutls` is currently not build for KaOS, but the PKGBUILD can be found [in this repository](https://github.com/wrajaka/kcp-libcurl-gnutls/blob/master/PKGBUILD) and has [to be build](https://kaosx.us/docs/package/#building-a-package) manually and installed prior as a dependency with `--asdeps`.

### Install:
```
kcp -i gitkraken
```
