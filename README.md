# Docker и Docker Compose

<div align="center">
  <img src="https://img.shields.io/badge/Docker-19.03.13-blue?style=flat" />
  <img src="https://img.shields.io/badge/Docker%20Compose-1.27.4-blue?style=flat" />
  <img src="https://img.shields.io/badge/release-v1.0.0-beta.1-blue?style=flat" />
  <img src="https://img.shields.io/badge/dev_branch-development-blue?style=flat" />
  <img src="https://img.shields.io/badge/license-MIT-blue?style=flat" />
</div>

**Этот репозиторий представляет собой bash-скрипт для максимально простой установке Docker и Docker Compose**

--- 

**Docker** - это платформа для разработки, доставки и запуска приложений в контейнерах. Контейнеры позволяют
разработчикам упаковывать приложения со всем необходимым программным обеспечением в единообразные блоки, которые могут
быть перенесены на любую совместимую систему, и которые можно запустить без необходимости настройки и перенастройки

**Docker Compose** - это инструмент для определения и запуска многоконтейнерных Docker-приложений. С помощью Compose Вы
можете использовать файл YAML для настройки сервисов вашего приложения. Затем с помощью одной команды Вы создаете и
запускаете все сервисы из Вашего конфигурационного файла

## Требования к системе

--- 

- Операционная система: Linux
    * Ubuntu
    * Debian
    * и другие форки этих дистрибутивов
- Установленный пакетный менеджер: apt

## Установка

---

**1. Скачайте скрипт установки Docker:**

#### Через `wget`

```sh
wget https://raw.githubusercontent.com/saydov/install-docker/master/install-docker
```

#### Через `curl`

```sh
curl -O https://raw.githubusercontent.com/saydov/install-docker/master/install-docker
```

**2. Добавьте права на выполнение:**

```sh
chmod +x install-docker
```

**3. Запустите скрипт установки:**

```sh
./install-docker
```

**4. Проверьте версию Docker:**

```sh
docker --version
```

## Готовые примеры Dockerfile и Docker Compose

---

- [Ubuntu](https://github.com/saydov/install-docker/tree/master/examples/ubuntu)
- [Redis](https://github.com/saydov/install-docker/tree/master/examples/redis)
- [RabbitMQ](https://github.com/saydov/install-docker/tree/master/examples/rabbitmq)

---

## Планы по продвижению репозитория

---

- [ ] Реализовать поддержку под Windows
- [ ] Добавить больше примеров (Debian, различные БД и веб-серверы)

## Полезные ссылки

---

- [Документация Docker](https://docs.docker.com)
- [Документация Docker Compose](https://docs.docker.com/compose/)

---
