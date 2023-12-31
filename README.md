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

How to enable [Gitea Actions](https://docs.gitea.com/usage/actions/quickstart). open `config/app.ini` file. add following lines.

```ini
[actions]
ENABLED=true

[webhook]
ALLOWED_HOST_LIST = your_server_ip
```

## Start Gitea Runner

Start Global Gitea Runner

```sh
cd gitea && mkdir -p data/act_runner
cd gitea && chmod 777 data/act_runner
cd gitea && docker-compose up -d gitea-runner
```

Start User's Gitea Runner

```sh
cd gitea && mkdir -p data/act_user_runner
cd gitea && chmod 777 data/act_user_runner
cd gitea && docker-compose up -d gitea-user-runner
```
