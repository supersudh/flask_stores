## Run Dockerfile locally

### Build the image

```
docker build -t flask-smorest-api .
```

### Daemonize the container

```
docker run -dp 5005:5000 -w /app -v "$(pwd):/app" flask-smorest-api sh -c "flask run --host 0.0.0.0"
```