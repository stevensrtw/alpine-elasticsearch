![es-logo](https://cdn.iconscout.com/icon/free/png-256/free-elastic-283142.png?f=webp&w=256)

# docker-elasticsearch-alpine



Alpine Linux based [Elasticsearch](https://www.elastic.co/products/elasticsearch) Docker Image

**Table of Contents**

- [docker-elasticsearch-alpine](#docker-elasticsearch-alpine)
  - [Why?](#why)
  - [Dependencies](#dependencies)
  - [Image Tags](#image-tags)
  - [Getting Started](#getting-started)
  - [Documentation](#documentation)
  - [Known Issues :warning:](#known-issues-warning)
  - [Issues](#issues)
  - [Credits](#credits)
  - [License](#license)

## Why?

Compare Image Sizes:

* official elasticsearch = 791.6 MB
* stevensrtw/elasticsearch = 447.28 MB

**version is 518 MB smaller !**

## Dependencies

* [alpine:latest](https://hub.docker.com/_/alpine/)

## Image Tags

``` bash
REPOSITORY               TAG                 SIZE
stevensrtw/elasticsearch   latest              1.02GB
stevensrtw/elasticsearch   8.1                 1.02GB
stevensrtw/elasticsearch   8.0                 1.02GB
stevensrtw/elasticsearch   7.17                411MB

```

## Getting Started

``` bash
$ docker run -d --name elastic -p 9200:9200 stevensrtw/elasticsearch
```

## Documentation

* [To create an elasticsearch cluster](docs/create.md)
* [To increase the HEAP_SIZE to 2GB](docs/options.md)
* [To monitor the clusters metrics using dockerbeat](docs/dockerbeat.md)
* [To run in production](docs/production.md)

## Known Issues :warning:

I have noticed when running the new **5.0+** version on a linux host you need to increase the memory map areas with the following command

``` bash
sudo sysctl -w vm.max_map_count=262144
```

## Issues

Find a bug? Want more features? Find something missing in the documentation? Let me know! Please don't hesitate to [file an issue](https://github.com/stevensrtw/docker-elasticsearch-alpine/issues/new)

## Credits

Heavily (if not entirely) influenced by https://github.com/docker-library/elasticsearch<br> Production docs from https://stefanprodan.com/2016/elasticsearch-cluster-with-docker/

## License

MIT Copyright (c) 2016-2022 **stevensrtw**