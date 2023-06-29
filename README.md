# keycloakTest

Обучение keycloak

## Установка окружения

Для работы keycloak понадобится база данных. Я буду использовать postgresql.
Запускать все приложения буду в docker.

Так же для запуска всех приложений я буду использовать docker compose

### Пример docker-compose

В этом примере используются два сервиса: keycloak и db. keycloak использует образ jboss/keycloak для запуска Keycloak, а db использует образ postgres для запуска PostgreSQL.

keycloak настраивается для работы на порту 8080 и устанавливает переменные среды KEYCLOAK_USER и KEYCLOAK_PASSWORD для настройки учетных данных администратора Keycloak.

db настраивается для работы на порту 5432 и устанавливает переменные среды POSTGRES_DB, POSTGRES_USER и POSTGRES_PASSWORD для настройки базы данных PostgreSQL.

Оба сервиса объединены в сеть keycloak_network, чтобы они могли взаимодействовать друг с другом.

В файле также определена секция volumes, которая монтирует локальную директорию ./data внутрь контейнера базы данных, чтобы сохранить данные PostgreSQL между запусками контейнеров.

Вы можете сохранить этот файл как docker-compose.yml и запустить команду docker-compose up в каталоге, где находится файл, чтобы запустить Keycloak и PostgreSQL с помощью Docker Compose.

#### Запуск docker-compose

Запустите команду `docker-compose up` в каталоге, где находится файл docker-compose.yml, чтобы запустить Keycloak и PostgreSQL с помощью Docker Compose.

```sh
docker-compose up
```
