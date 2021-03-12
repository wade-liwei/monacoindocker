


# from https://github.com/blocknetdx/dockerimages/blob/monacoin-monacoin-0.17.1/mona/Dockerfile






343  sudo  docker run -d --name=mona -p 9401:9401 -v=/data/monacoin/config:/opt/blockchain/config -v=/data/monacoin/data:/opt/blockchain/data  blocknetdx/monacoin:monacoin-0.17.1   monacoind -daemon=0 -rpcuser= -rpcpassword=123



docker build --build-arg cores=8 -t wade/mona:0.0.1 .
