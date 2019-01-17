# docker-zold
Docker container for [Zold](http://zold.io/) cryptocurrency node

Run as 
```
docker build . -t zold-node
docker run -d -p 4096:4096 zold-node /node.sh --host=<your host IP> --invoice=17737fee5b825835
```
Replace 17737fee5b825835 with your wallet id and provide your host ip address.

To save zold data (remote nodes addresses, wallet files, scores) create a volume
```
docker volume create zold 
docker run -d -p 4096:4096 -v zold:/zold zold-node /node.sh --host=<your host IP> --invoice=17737fee5b825835
```
