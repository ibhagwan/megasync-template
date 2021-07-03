## Void Linux template file for xbps-src

Instructions for building latest `MEGAsync` on void linux using `xbps-src`:

1. Setup the `void-packages` repo:

```sh
❯ git clone --depth=1 https://github.com/void-linux/void-packages
❯ cd void-packages
❯ ./xbps-src binary-bootstrap
❯ echo XBPS_ALLOW_RESTRICTED=yes >> etc/conf
```

2. Clone the template repo into `srcpkgs`:

```sh
❯ rm -rf ./srcpkgs/MEGAsync
❯ git clone https://github.com/ibhagwan/megasync-template.git ./srcpkgs/MEGAsync
```

3. Build & install the package:

```sh
❯ ./xbps-src pkg MEGAsync
❯ sudo xbps-install --repository=hostdir/binpkgs MEGAsync 
```
