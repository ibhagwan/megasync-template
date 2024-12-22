## Void Linux template file for xbps-src

This package is primarily maintained on [cereus-pkgs](https://codeberg.org/cereus-linux/cereus-pkgs/src/branch/master/srcpkgs/megasync) repository but it's mirrored here too for Void Linux users convenience.

Instructions for building latest `megasync` on Void Linux using `xbps-src`:

1. Setup the `void-packages` repo:

```sh
❯ git clone --depth=1 https://github.com/void-linux/void-packages
❯ cd void-packages
❯ ./xbps-src binary-bootstrap
❯ echo XBPS_ALLOW_RESTRICTED=yes >> etc/conf
```

2. Clone the template repo into `srcpkgs`:

```sh
❯ git clone https://github.com/ibhagwan/megasync-template.git ./srcpkgs/megasync
```

3. Build & install the package:

```sh
❯ ./xbps-src pkg megasync
❯ sudo xbps-install --repository=hostdir/binpkgs/nonfree megasync
```
