# Setup Local Environment


## Spin up your DB with Docker
```bash
$ docker-compose up -d
```

## Running Without Docker(For Devs)
Make sure that PostgreSQL is up and running in your local, or you can run it via docker.

First install uv (python package nad project manager)
```bash
$ curl -LsSf https://astral.sh/uv/install.sh | sh
```

Install python3.13 using uv
```bash
$ uv python install 3.13.0
```

Create virtual environment and activate it
```bash
$ uv venv --python 3.13
$ source .venv/bin/activate
```

Install all dependencies

```bash
$ uv pip install -r pyproject.toml
```

Now you are ready to run the project. 
```bash
$ python manage.py runserver