# Build the image

```
docker build . -t mynodeapp:latest
```

# Running an app

```
docker run --rm mynodeapp:latest
```

# Versions

1. Change hello.js to output `This is version A`
2. `docker build . -t mynodeapp:versionA`
3. Change hello.js to output `This is version B`
4. `docker build . -t mynodeapp:versionB`

```
# Outputs: This is version A
docker run --rm mynodeapp:versionA


# Outputs: this is version B
docker run --rm mynodeapp:versionB
```