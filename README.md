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

## Start Gitea Runner

```sh
cd gitea && docker-compose up -d gitea-runner
```
