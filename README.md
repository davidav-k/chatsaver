# ChatSaver — a microservice application for archiving information from a browser

---

## Description

ChatSaver is a system for archiving information from a given browser tab and saving it to a local database with subsequent access via API or Web interface.

---

## Technologies

### Backend:
- Java 21
- Spring Boot 3
- Spring Cloud: Eureka, Config Server, Gateway
- Spring JPA (Hibernate)
- PostgreSQL
- Docker / Docker Compose

### Frontend:
- Vue 3 + Vite
- Pinia / Vue Router / Axios
- Docker (Nginx)

---

### Requirements:
- Docker and Docker Compose installed
- Git

### Installation and launch:

git clone https://github.com/.../chatsaver.git
cd chatsaver
cp .env.example .env # or configure .env manually
docker compose -f docker/compose.yml up --build

After launch:
- Gateway: http://localhost:8080
- Frontend (if running separately): http://localhost:5173
- Eureka Dashboard: http://localhost:8761

---


# ChatSaver — микросервисное приложение для архивации информации из браузера

---

## Описание

ChatSaver — это система для архивации информации из заданной вкладки браузера и сохранения ее в локальную базу данных с последующим доступом по API или по Веб-интерфейсу.

---

## Технологии

### Backend:
- Java 21
- Spring Boot 3
- Spring Cloud: Eureka, Config Server, Gateway
- Spring JPA (Hibernate)
- PostgreSQL
- Docker / Docker Compose

### Frontend:
- Vue 3 + Vite
- Pinia / Vue Router / Axios
- Docker (Nginx)

---

## Быстрый старт

### Требования:
- Установленные Docker и Docker Compose
- Git

### Установка и запуск:

    git clone https://github.com/.../chatsaver.git
    cd chatsaver
    cp .env.example .env   # или выполнить настройку .env вручную
    docker compose -f docker/compose.yml up --build

После запуска:
- Gateway: http://localhost:8080
- Frontend (если поднят отдельно): http://localhost:5173
- Eureka Dashboard: http://localhost:8761

---
