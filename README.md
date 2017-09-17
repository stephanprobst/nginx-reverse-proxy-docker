# NGINX Reverse Proxy Using Docker

Simple example for url routing and port routing:

Run following commands to publish sites independent:

```bash
docker-compose -f site1/docker-compose.yml up -d
docker-compose -f site2/docker-compose.yml up -d
```

Then run:
```bash
docker-compose -f proxy/docker-compose.yml up -d
```

Open:

```
http://localhost/site1/
http://localhost/site2/
```
or
```
http://localhost:81/
```

For stack deploy:
```bash
docker stack deploy -c docker-compose.stack.yml reverse
```

Base Code from:

This code is from the [article](http://linoxide.com/containers/setup-nginx-reverse-proxy-docker/)