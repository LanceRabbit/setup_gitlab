# Gitlab

## setup setting

### copy env file

```shell
cp env.example .env
```

### setup env

use openssl for generate the random variables.

```shell
openssl rand -base64 64
```

```yml
HOST=
PORT=
SSH_PORT=
GITLAB_ROOT_PASSWORD=
GITLAB_ROOT_EMAIL=
DB_USERNAME=
DB_PASSWORD=
DB_NAME=
GITLAB_SECRETS_DB_KEY_BASE=
GITLAB_SECRETS_SECRET_KEY_BASE=
GITLAB_SECRETS_OTP_KEY_BASE=
SMTP_ENABLED=
SMTP_DOMAIN=
SMTP_HOST=
SMTP_PORT=
SMTP_USER=
SMTP_PASS=
```

## run

```shell
docker-compose up
```

## setup Gitlab runner

go to `admin/runners` panel get the registration token.

replace the url `your_url`

```shell
docker exec -it [Runner-container] gitlab-runner register --url your_url --registration-token [Token]
```
