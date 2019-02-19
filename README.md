# docker-zold
Docker container for [Zold](http://zold.io/) cryptocurrency node

Run from docker hub container pin2t/zold

```
docker run -d -p 4096:4096 pin2t/zold:latest /node.sh --host=<your host IP> --invoice=fb166bda83dff5a3
```
Replace fb166bda83dff5a3 with your wallet id and provide your host ip address.

To save zold data (remote nodes addresses, wallet files, scores) create a volume
```
docker volume create zold 
docker run -d -p 4096:4096 -v zold:/zold pin2t/zold:latest /node.sh --host=<your host IP> --invoice=fb166bda83dff5a3
```

Run from repo https://github.com/pin2t/docker-zold 
```
docker build . -t zold-node
docker run -d -p 4096:4096 zold-node /node.sh --host=<your host IP> --invoice=fb166bda83dff5a3
```


