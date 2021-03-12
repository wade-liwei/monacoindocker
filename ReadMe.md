1. from https://github.com/blocknetdx/dockerimages/blob/monacoin-monacoin-0.17.1/mona/Dockerfile



2. run with volume
 sudo  docker run -d --name=mona -p 9401:9401 -v=/data/monacoin/config:/opt/blockchain/config -v=/data/monacoin/data:/opt/blockchain/data  blocknetdx/monacoin:monacoin-0.17.1   monacoind -daemon=0 -rpcuser= -rpcpassword=123



3. build docker image cmd

```
 docker build --build-arg cores=8 -t wade/mona:0.0.1 .

```


4. startup

```

使用docker image 里的 cmd启动
 sudo  docker run -d --name=mona-self-1 -p 9402:9402  -v=/data/monacoin-self/data:/opt/blockchain/data  self-monacoin-1


替换docker image里的cmd参数
monacoind -daemon=0 -rpcuser=user -rpcpassword=pass -rpcbind=0.0.0.0 -rpcallowip=0.0.0.0/0

```


6. info cmd 

```
 curl --user monacoin:20210312 --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockchaininfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9402/
```
