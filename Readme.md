# Ethereum Development Environment

## Truffle Environment

Truffle Docker Environment is defined by **truffle/Dockerfile**
This is a docker image for easy development in Ethereum Solidity. This image supports:

 * Truffle,
 * zeppelin-solidity
 * and Ganache.

### Build image

```bash
docker build -t eth-dev-truffle:0.0.1 truffle
```


### Run

```bash
docker run -ti --rm -v ~/workdir:/root/workdir eth-dev-truffle:0.0.1
```


## Populus Environment

Populus Docker Enviroment is defined by **populus/Dockerfile**
This is a docker image for easy development in Ethereum Solidity. This image supports:

 * python 3.6.3-r9,
 * openssl 1.0.2o-r0
 * pip,
 * populus 2.2.0

### Build image

```bash
docker build -t eth-dev-populus:0.0.1 populus
```


### Run

```bash
docker run -ti --rm -v ~/workdir:/root/workdir eth-dev-populus:0.0.1
```
