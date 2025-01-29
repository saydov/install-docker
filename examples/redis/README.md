# Установка Redis в Docker

**Redis** — это высокопроизводительная система управления базами данных, которая использует память для хранения данных

Есть два способа установки **Redis** в **Docker**:
- [Dockerfile](#-dockerfile)
- [Docker Compose](#-docker-compose)

---

## ⭐ Dockerfile

**1. Скачайте `Dockerfile` из репозитория:**
   #### Через `wget`
   ```sh
   wget https://raw.githubusercontent.com/saydov/docker/main/examples/redis/Dockerfile
   ```
   #### Через `curl`
   ```sh
   curl -O https://raw.githubusercontent.com/saydov/docker/main/examples/redis/Dockerfile
   ```

**2. Соберите образ:**
   ```sh
   docker build -t redis-img .
   ```

**3. Запустите контейнер:**
   ```sh
   docker run -d -p 6379:6379 --name redis-server redis-img
   ```

**4. Проверьте, что контейнер работает:**
   ```sh
   docker ps
   ```

**5. Подключитесь к Redis через CLI:**
   ```sh
   docker exec -it redis-server redis-cli
   ```

**6. Остановка контейнера:**
   ```sh
   docker stop redis-server
   ```

**7. Удаление контейнера:**
   ```sh
   docker rm redis-server
   ```

**8. Удаление образа:**
   ```sh
   docker rmi redis-img
   ```

---

## ⭐ Docker Compose

**1. Скачайте `docker-compose.yml` из репозитория:**
#### Через `wget`
   ```sh
   wget https://raw.githubusercontent.com/saydov/docker/main/examples/redis/docker-compose.yml
   ```
#### Через `curl`
   ```sh
   curl -O https://raw.githubusercontent.com/saydov/docker/main/examples/redis/docker-compose.yml
   ```

**2. Соберите контейнеры:**
   ```sh
   docker-compose build
   ```

**3. Запустите контейнеры:**
   ```sh
   docker-compose up -d
   ```

**4. Проверьте, что контейнеры работает:**
   ```sh
   docker-compose ps
   ```

  или 

  ```sh
  docker ps
  ```

**5. Подключитесь к Redis через CLI:**
   ```sh
   docker-compose exec redis-server redis-cli
   ```

**6. Остановка контейнера:**
   ```sh
   docker-compose down
   ```

**7. Удаление контейнеров:**
   ```sh
   docker-compose rm
   ```
---

## Полезные ссылки

- [Документация Redis](https://redis.io/documentation)
- [Документация Docker](https://docs.docker.com)
- [Документация Docker Compose](https://docs.docker.com/compose/)

---