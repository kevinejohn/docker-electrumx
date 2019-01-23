
# docker-electrumx

[![Build Status](https://travis-ci.org/kevinejohn/docker-electrumx.svg?branch=master)](https://travis-ci.org/kevinejohn/docker-electrumx)
[![Image Layers](https://images.microbadger.com/badges/image/kevinejohn/electrumx.svg)](https://microbadger.com/images/kevinejohn/electrumx)
[![Docker Pulls](https://img.shields.io/docker/pulls/kevinejohn/electrumx.svg)](https://hub.docker.com/r/kevinejohn/electrumx/)

> Run an Electrum server with one command

An easily configurable Docker image for running an Electrum server.

## Usage

```
docker run \
  -v /home/username/electrumx:/data \
  -e DAEMON_URL=http://user:pass@host:port \
  -e COIN=BitcoinSV \
  -p 50002:50002 \
  kevinejohn/electrumx
```

If there's an SSL certificate/key (`electrumx.crt`/`electrumx.key`) in the `/data` volume it'll be used. If not, one will be generated for you.

You can view all ElectrumX environment variables here: https://github.com/kyuupichan/electrumx/blob/master/docs/environment.rst

### TCP Port

By default only the SSL port is exposed. You can expose the unencrypted TCP port with `-p 50001:50001`, although this is strongly discouraged.

## License

MIT © Luke Childs
