# Example 1. Check node version

```
docker run --rm \
    node:8 \
    node --version
```

# Running an app

## Will not work
```
docker run --rm \
    node:8 \
    node hello.js
```

## Will work
```
docker run --rm \
    -v $(pwd):/app \
    node:8 \
    node /app/hello.js
```

```
docker run --rm \
    -v $(pwd)/hello.js:/hello.js \
    node:8 \
    node hello.js
```


