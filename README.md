Sentiment analysis docker image for simplified setup

# Install

Pull images

```shell
git clone https://github.com/LiveHelperChat/sentiment && cd sentiment
docker-compose -f docker-compose.yml pull
wget https://livehelperchat.com/var/deep.tgz
tar zxfv deep.tgz
rm -f deep.tgz
```

Run one time

```
docker-compose -f docker-compose.yml up
```

Run as a service

```
docker-compose -f docker-compose.yml up -d
```

Testing

```
curl -X POST "http://localhost:5000/model" -H "accept: application/json" -H "Content-Type: application/json" -d "{\"x\":[\"all went no so good, but could have been better\"]}"
```

For Live Helper Chat configuration read manual here (will be updated)
