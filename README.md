# docker-zold
Docker container for [Zold](http://zold.io/) cryptocurrency node

Run from docker hub container pin2t/zold

```
docker run -d -p 4096:4096 pin2t/zold:latest /node.sh --host=<your host IP> --invoice=17737fee5b825835
```
Replace 17737fee5b825835 with your wallet id and provide your host ip address.

To save zold data (remote nodes addresses, wallet files, scores) create a volume
```
docker volume create zold 
docker run -d -p 4096:4096 -v zold:/zold pin2t/zold:latest /node.sh --host=<your host IP> --invoice=17737fee5b825835
```

Run from repo https://github.com/pin2t/docker-zold 
```
docker build . -t zold-node
docker run -d -p 4096:4096 zold-node /node.sh --host=<your host IP> --invoice=17737fee5b825835
```


