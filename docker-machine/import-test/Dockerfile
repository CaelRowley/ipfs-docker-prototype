FROM hyperledger/fabric-tools 

RUN apt-get update
RUN apt-get install -y wget
RUN apt-get install -y golang-go

# install ipfs
RUN wget https://dist.ipfs.io/go-ipfs/v0.4.13/go-ipfs_v0.4.13_linux-amd64.tar.gz
RUN tar xvfz go-ipfs_v0.4.13_linux-amd64.tar.gz
WORKDIR /go-ipfs
RUN ./install.sh
