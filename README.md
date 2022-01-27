# Docker Laravel

php version: 8.1.2

## Installation

1. Create "src" folder and put your laravel project in this folder

2. Open docker-compose.yml file and nginx & mysql ports to the ones you need

3. Change mysql credentials in docker-compose.yml to the ones you need

4. Enter src folder and type:

```bash
cp .env.example .env
```

5. Change .env database credentials and port to ones you wrote

6. Run the following commands at the root of the project:


```bash
docker-compose build --build-arg USER_ID=$(id -u) --build-arg GROUP_ID=$(id -g)
docker-compose up -d
docker-compose run artisan key:generate
docker-compose restart
```

Application is ready