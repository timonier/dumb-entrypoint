# README

Sets of entrypoints for Linux containers

## Installation

### dumb-entrypoint

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/local/sbin

# Use local installation

sudo src/dumb-entrypoint/installer install

# Use remote installation

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | sudo sh -s -- install
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

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-init/installer" | sudo sh -s -- install
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `dumb-init` will be installed in `/usr/sbin`.

### gosu

```sh
# Define installation folder

export INSTALL_DIRECTORY=/usr/local/sbin

# Use local installation

sudo src/gosu/installer install

# Use remote installation

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | sudo sh -s -- install
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `gosu` will be installed in `/usr/sbin`.

### s6-overlay

```sh
# Use local installation

sudo src/s6-overlay/installer install

# Use remote installation

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/s6-overlay/installer" | sudo sh -s -- install
```

__Note 1__: It is not possible to change the installation folder.

__Note 2__: It is not possible to remove `s6-overlay`.

__Note__: If you do not define `INSTALL_DIRECTORY`, `gosu` will be installed in `/usr/sbin`.

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

If you like / use this project, please let me known by adding a [★](https://help.github.com/articles/about-stars/) on the [GitHub repository](https://github.com/timonier/dumb-entrypoint).

## Links

* [just-containers/s6-overlay](https://github.com/just-containers/s6-overlay)
* [localedef](http://manpages.ubuntu.com/manpages/latest/man1/localedef.1.html)
* [tianon/gosu](https://github.com/tianon/gosu)
* [timonier/version-lister](https://github.com/timonier/version-lister)
* [yelp/dumb-init](https://github.com/Yelp/dumb-init)
