# Ethereum Development Environment

## Truffle Environment

Truffle Docker Environment is defined by **truffle/Dockerfile**
This is a docker image for easy development in Ethereum Solidity. This image supports:

 * Truffle (),
 * zeppelin-solidity (1.10.0)
 * Ganache (v6.1.6 ganache-core: 2.1.5)
 * solc (Version: 0.4.24+commit.e67f0147.Linux.g++)
 * git
 * openssl

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
