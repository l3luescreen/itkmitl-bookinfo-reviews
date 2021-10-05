# itkmitl-bookinfo-reviews

## Build

```bash
docker build -t reviews .
```

## Run
```bash
docker run -d --rm -p 8082:9080 --name reviews-service --link ratings:ratings -e 'RATINGS_SERVICE=http://ratings:8080' -e ENABLE_RATINGS="true" reviews
```