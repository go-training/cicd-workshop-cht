# cicd-workshop-cht

CI/CD workshop

## Prepare

```sh
mkdir -p gitea/{data,config}
cd gitea
touch docker-compose.yml
# chnage permission
chmod 777 config/ data/
```

## Start Gitea Server

```sh
cd gitea && docker-compose up -d gitea-server
```

How to enable gitea actions. open `config/app.ini` file. add following lines.

```ini
[actions]
ENABLED=true
```

## Start Gitea Runner

```sh
cd gitea && docker-compose up -d gitea-runner
```
