# README

Minimal entrypoint for Linux containers

## Installation

* Copy `src/dumb-entrypoint` into an executable folder (like `/usr/local/sbin`).
* Install [yelp/dumb-init](https://github.com/Yelp/dumb-init) into an executable folder (like `/usr/local/sbin`).
* Install [tianon/gosu](https://github.com/tianon/gosu) into an executable folder (like `/usr/local/sbin`).

Linux users can use the [installer](https://github.com/timonier/dumb-entrypoint/blob/master/bin/installer):

```sh
curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | sudo sh -s -- install
# Install scripts into "/usr/local/sbin"

curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | sudo INSTALL_DIRECTORY="/usr/sbin" sh -s -- install
# Install scripts into "/usr/sbin"
```

## Usage

* Mount `dumb-entrypoint`, `dumb-init` and `gosu` into the container (or mount the executable folder).
* Use `dumb-init` as entrypoint.
* Prefix your command by `dumb-entrypoint`.

```sh
docker run \
    --entrypoint dumb-init \
    $(env | cut -d= -f1 | awk '{print "--env", $1}') \
    --volume /etc/passwd:/etc/passwd:ro \
    --volume $(which dumb-entrypoint):/usr/local/sbin/dumb-entrypoint:ro \
    --volume $(which dumb-init):/usr/local/sbin/dumb-init:ro \
    --volume $(which gosu):/usr/local/sbin/gosu:ro \
    ubuntu:latest dumb-entrypoint printenv
```

## Contributing

1. Fork it.
2. Create your branch: `git checkout -b my-new-feature`.
3. Commit your changes: `git commit -am 'Add some feature'`.
4. Push to the branch: `git push origin my-new-feature`.
5. Submit a pull request.

## Links

* [localedef](http://manpages.ubuntu.com/manpages/latest/man1/localedef.1.html)
* [tianon/gosu](https://github.com/tianon/gosu)
* [timonier/version-lister](https://github.com/timonier/version-lister)
* [yelp/dumb-init](https://github.com/Yelp/dumb-init)
