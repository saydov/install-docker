# Установка RabbitMQ в Docker

**RabbitMQ** — это программное обеспечение с открытым исходным кодом, которое реализует адаптер сообщений AMQP (Advanced Message Queuing Protocol)

Есть два способа установки **RabbitMQ** в **Docker**:
- [Dockerfile](#-dockerfile)
- [Docker Compose](#-docker-compose)

---

## ⭐ Dockerfile

**1. Скачайте `Dockerfile` из репозитория:**
#### Через `wget`
   ```sh
   wget https://raw.githubusercontent.com/saydov/install-docker/master/examples/rabbitmq/Dockerfile
   ```
#### Через `curl`
   ```sh
   curl -O https://raw.githubusercontent.com/saydov/install-docker/master/examples/rabbitmq/Dockerfile
   ```

**2. Соберите образ:**
   ```sh
   docker build -t rabbitmq-img .
   ```

**3. Запустите контейнер:**
   ```sh
   docker run -d -p 5672:5672 --name rabbitmq-server rabbitmq-img
   ```

**4. Проверьте, что контейнер работает:**
   ```sh
   docker ps
   ```

**5. Остановка контейнера:**
   ```sh
   docker stop rabbitmq-server
   ```

**6. Удаление контейнера:**
   ```sh
   docker rm rabbitmq-server
   ```

**7. Удаление образа:**
   ```sh
   docker rmi rabbitmq-img
   ```

---

## ⭐ Docker Compose

**1. Скачайте `docker-compose.yml` из репозитория:**
#### Через `wget`
   ```sh
   wget https://raw.githubusercontent.com/saydov/install-docker/master/examples/rabbitmq/docker-compose.yml
   ```
#### Через `curl`
   ```sh
   curl -O https://raw.githubusercontent.com/saydov/install-docker/master/examples/rabbitmq/docker-compose.yml
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

**5. Остановка контейнера:**
   ```sh
   docker-compose down
   ```

**6. Удаление контейнеров:**
   ```sh
   docker-compose rm
   ```
---

## Полезные ссылки

- [Документация RabbitMQ](https://www.rabbitmq.com/documentation.html)

---