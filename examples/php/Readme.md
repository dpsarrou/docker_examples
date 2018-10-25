# Example 1. Check node version

```
docker run --rm \
    php:7-cli \
    php --version
```

# File sharing

## Will not work
```
docker run --rm \
    php:7-cli \
    php hello.php
```

## Will work
```
docker run --rm \
    -v $(pwd)/hello.php:/hello.php \
    php:7-cli \
    php hello.php
```


