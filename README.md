## Venv commands

```
python3 -m venv .venv
[Close terminal session in VSCODE and Press Cmd + J]
pip install -r requirements.txt
flask run
```

## Run Dockerfile locally

### Build the image

```
docker build -t flask-smorest-api .
```

### Daemonize the container

```
docker run -dp 5005:5000 -w /app -v "$(pwd):/app" flask-smorest-api sh -c "flask run --host 0.0.0.0"
```

## Migrations

```
flask db init
flask db migrate
flask db upgrade
```