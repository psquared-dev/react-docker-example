A sample projec to deploy react based app on nginx

## How to run

For Development:

```bash
docker build -t tracker_prod -f Dockerfile.dev .
docker run -it -v /app/node_modules -v $PWD:/app -p 3000:3000 tracker_prod
```

For Production:

```bash
docker build -t tracker_prod .
docker run -it -v /app/node_modules -v $PWD:/app -p 3000:80 tracker_prod
```
