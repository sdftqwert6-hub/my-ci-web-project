# My Web Project

Простой статический сайт для практической работы с Docker.

## Сборка образа

```powershell
docker build -t my-web-site .
```

## Запуск на порту 8080

```powershell
docker run -d -p 8080:80 --name web-port-test my-web-site
```

Откройте http://localhost:8080

## Запуск с переменными окружения

```powershell
docker run -d -p 8082:80 --env-file .env --name web-env-test my-web-site
docker exec web-env-test printenv
```

Для второго этапа измените значения в `.env` и создайте новый контейнер с другим именем и портом.
