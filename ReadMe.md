# from https://github.com/blocknetdx/dockerimages/blob/monacoin-monacoin-0.17.1/mona/Dockerfile



会覆盖调本地的存储
 sudo  docker run -d --name=mona -p 9401:9401 -v=/data/monacoin/config:/opt/blockchain/config -v=/data/monacoin/data:/opt/blockchain/data  blocknetdx/monacoin:monacoin-0.17.1   monacoind -daemon=0 -rpcuser= -rpcpassword=123



docker build --build-arg cores=8 -t wade/mona:0.0.1 .



self-monacoin



sudo  docker run -d --name=mona-self-1 -p 9402:9402  -v=/data/monacoin-self/data:/opt/blockchain/data  self-monacoin-1



monacoind -daemon=0 -rpcuser=user -rpcpassword=pass -rpcbind=0.0.0.0 -rpcallowip=0.0.0.0/0




curl --user monacoin:20210312 --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockchaininfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9402/
