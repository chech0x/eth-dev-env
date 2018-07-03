# Ethereum Development Enviroment
This is a docker image for easy development in Ethereum Solidity with Truffle and Ganache.

## Build image

```bash
docker build -t eth-dev-env:0.0.1 .
```


## Run

```bash
docker run -ti --rm -v ~/workdir:/root/workdir eth-dev-env:0.0.1
```
