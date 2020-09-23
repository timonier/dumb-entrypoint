# README

Sets of entrypoints for Linux containers

⚠️ This project is no longer maintained. ⚠️

## Installation

### dockerize

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/local/bin

# Use local installation

sudo src/dockerize/installer install

# Use remote installation

curl --location "https://gitlab.com/timonier/dumb-entrypoint/raw/master/src/dockerize/installer" | sudo sh -s -- install
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `dockerize` will be installed in `/usr/sbin`.

### dumb-entrypoint

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/local/sbin

# Use local installation

sudo src/dumb-entrypoint/installer install

# Use remote installation

curl --location "https://gitlab.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | sudo sh -s -- install
```

__Note 1__: If you do not define `INSTALL_DIRECTORY`, `dumb-entrypoint` will be installed in `/usr/sbin`.

__Note 2__: `gosu` is required by `dumb-entrypoint`.

### dumb-init

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/local/sbin

# Use local installation

sudo src/dumb-init/installer install

# Use remote installation

curl --location "https://gitlab.com/timonier/dumb-entrypoint/raw/master/src/dumb-init/installer" | sudo sh -s -- install
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `dumb-init` will be installed in `/usr/sbin`.

### gosu

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/local/sbin

# Use local installation

sudo src/gosu/installer install

# Use remote installation

curl --location "https://gitlab.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | sudo sh -s -- install
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `gosu` will be installed in `/usr/sbin`.

### s6-overlay

```sh
# Use local installation

sudo src/s6-overlay/installer install

# Use remote installation

curl --location "https://gitlab.com/timonier/dumb-entrypoint/raw/master/src/s6-overlay/installer" | sudo sh -s -- install
```

__Note 1__: It is not possible to change the installation folder.

__Note 2__: It is not possible to remove `s6-overlay`.

## Links

* [just-containers/s6-overlay](https://github.com/just-containers/s6-overlay)
* [jwilder/dockerize](https://github.com/jwilder/dockerize)
* [localedef](http://manpages.ubuntu.com/manpages/latest/man1/localedef.1.html)
* [tianon/gosu](https://github.com/tianon/gosu)
* [timonier/version-lister](https://gitlab.com/timonier/version-lister)
* [yelp/dumb-init](https://github.com/Yelp/dumb-init)
