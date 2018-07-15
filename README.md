# README

Sets of entrypoints for Linux containers

## Installation

### dumb-entrypoint

```sh
# Define installation folder

export INSTALL_DIRECTORY="/usr/sbin"

# Install gosu (requires by dumb-entrypoint)

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | sh -s -- install

# Install dumb-entrypoint

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | sh -s -- install

# Remove dumb-entrypoint

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | sh -s -- uninstall
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `dumb-entrypoint` will be installed in `/usr/local/sbin`.

### dumb-init

```sh
# Define installation folder

export INSTALL_DIRECTORY="/usr/sbin"

# Install gosu

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-init/installer" | sh -s -- install

# Remove gosu

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-init/installer" | sh -s -- uninstall
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `dumb-init` will be installed in `/usr/local/sbin`.

### gosu

```sh
# Define installation folder

export INSTALL_DIRECTORY="/usr/sbin"

# Install gosu

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | sh -s -- install

# Remove gosu

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | sh -s -- uninstall
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `gosu` will be installed in `/usr/local/sbin`.

### s6-overlay

```sh
# Install s6-overlay

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/s6-overlay/installer" | sh -s -- install
```

__Note 1__: It is not possible to change the installation folder.

__Note 2__: It is not possible to remove `s6-overlay`.

### syslog-stdout

```sh
# Define installation folder

export INSTALL_DIRECTORY="/usr/sbin"

# Install syslog-stdout

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/syslog-stdout/installer" | sh -s -- install

# Remove syslog-stdout

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/syslog-stdout/installer" | sh -s -- uninstall
```

__Note__: If you do not define `INSTALL_DIRECTORY`, `gosu` will be installed in `/usr/local/sbin`.

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
* [timonier/syslog-stdout](https://github.com/timonier/syslog-stdout)
* [timonier/version-lister](https://github.com/timonier/version-lister)
* [yelp/dumb-init](https://github.com/Yelp/dumb-init)
