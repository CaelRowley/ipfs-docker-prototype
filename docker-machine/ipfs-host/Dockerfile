FROM ubuntu

RUN apt-get update
RUN apt-get install -y wget
RUN apt-get install -y golang-go

# install ipfs
RUN wget https://dist.ipfs.io/go-ipfs/v0.4.13/go-ipfs_v0.4.13_linux-amd64.tar.gz
RUN tar xvfz go-ipfs_v0.4.13_linux-amd64.tar.gz
WORKDIR /go-ipfs
RUN ./install.sh


EXPOSE 80

# run ipfs download and then upload a picture
RUN ipfs init
RUN mkdir cat
WORKDIR /cat
RUN wget https://upload.wikimedia.org/wikipedia/commons/thumb/3/3a/Cat03.jpg/1200px-Cat03.jpg
RUN ipfs add -r .
RUN ipfs daemon