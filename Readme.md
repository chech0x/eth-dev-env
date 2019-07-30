# Ethereum Development Environment

## Truffle Environment

Truffle Docker Environment is defined by **truffle/Dockerfile**
This is a docker image for easy development in Ethereum Solidity. This image supports:

 * Truffle (v5.0.29),
 * Ganache (v6.5.0 (ganache-core: 2.6.0)s
 * solc (Version: 0.5.10+commit.5a6ea5b1.Linux.g++)
 * @openzeppelin/cli (2.5.2) (Openzeppelin SDK [ex **zos**])
 * git (2.22.0)
 * OpenSSL (1.1.1c  28 May 2019)

### Build image

```bash
docker build -t eth-dev-truffle:latest truffle
```


### Run

```bash
docker run -ti --rm -v ~/workdir:/root/workdir eth-truffle-dev:latest
```


## Populus Environment

Populus Docker Enviroment is defined by **populus/Dockerfile**
This is a docker image for easy development in Ethereum Solidity. This image supports:

 * python 3.6.3-r9,
 * openssl 1.0.2o-r0
 * pip,
 * populus 2.2.0
 * git

### Build image

```bash
docker build -t eth-populus-dev:latest populus
```


### Run

```bash
docker run -ti --rm -v ~/workdir:/root/workdir eth-populus-dev:latest
```
