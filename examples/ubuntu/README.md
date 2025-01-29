# Установка Ubuntu в Docker

Есть два способа установки **Ubuntu** в **Docker**:
- [Dockerfile](#-dockerfile)
- [Docker Compose](#-docker-compose)

---

## ⭐ Dockerfile

**1. Скачайте `Dockerfile` из репозитория:**
   #### Через `wget`
   ```sh
   wget https://raw.githubusercontent.com/saydov/install-docker/master/examples/ubuntu/Dockerfile
   ```
   #### Через `curl`
   ```sh
   curl -O https://raw.githubusercontent.com/saydov/install-docker/master/examples/ubuntu/Dockerfile
   ```

**2. Соберите образ:**
   ```sh
   docker build -t ubuntu-img .
   ```

**3. Запустите контейнер:**
   ```sh
   docker run -d --name ubuntu-container ubuntu-img
   ```

**4. Проверьте, что контейнер работает:**
   ```sh
   docker ps
   ```

**5. Подключитесь к контейнеру через оболочку /bin/bash:**
   ```sh
   docker exec -it ubuntu-container /bin/bash
   ```

**6. Остановка контейнера:**
   ```sh
   docker stop ubuntu-container
   ```

**7. Удаление контейнера:**
   ```sh
   docker rm ubuntu-container
   ```

**8. Удаление образа:**
   ```sh
   docker rmi ubuntu-img
   ```

---

## ⭐ Docker Compose

**1. Скачайте `docker-compose.yml` из репозитория:**
#### Через `wget`
   ```sh
   wget https://raw.githubusercontent.com/saydov/install-docker/master/examples/ubuntu/docker-compose.yml
   ```
#### Через `curl`
   ```sh
   curl -O https://raw.githubusercontent.com/saydov/install-docker/master/examples/ubuntu/docker-compose.yml
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

**5. Подключитесь к контейнеру через оболочку /bin/bash:**
   ```sh
   docker-compose exec ubuntu-container /bin/bash
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

- [Документация Ubuntu](https://ubuntu.com)

---