# GPlayCli on Docker

Run the project https://github.com/matlink/gplaycli inside a Docker container.
A pre-built image is available in dockerhub as lerignoux/gplaycli

## tldr
```
docker run --rm -v `pwd`:/dl -w /dl lerignoux/gplaycli gplaycli -c /dl/gplaycli.conf -d org.mozilla.focus
```

## Configuration
copy Fill the configuration template `gplaycli.tpl.conf` as `gplaycli.conf`

## Container Build
```
git clone git@github.com:rande/docker-gplaycli.git
cd docker-glaycli
docker build -t gplaycli .
```

## Advanced usage
  - Download an application
        `docker run --rm -v `pwd`:/dl -w /dl lerignoux/gplaycli gplaycli -c /dl/gplaycli.conf -d org.mozilla.focus`

  - Update APK
        `docker run --rm -v `pwd`:/dl -w /dl lerignoux/gplaycli gplaycli -c /dl/gplaycli.conf -u /dl`

  - Search
        `docker run --rm -v `pwd`:/dl -w /dl lerignoux/gplaycli gplaycli -c /dl/gplaycli.conf -s focus`

  - Help
        `docker run --rm -v `pwd`:/dl -w /dl lerignoux/gplaycli gplaycli -c /dl/gplaycli.conf --help`
