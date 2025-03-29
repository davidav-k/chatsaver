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

## Environment variables (.env)

# Database
POSTGRESQL_HOST=192.168.1.156
POSTGRESQL_DATABASE=gptchatsaver_db
POSTGRESQL_USERNAME=user
POSTGRESQL_PASSWORD=Password123
POSTGRESQL_PORT=5432

# Services
CONFIG_SERVER_URI=http://config-server:8888
EUREKA_URI=http://eureka-server:8761/eureka
GATEWAY_PORT=8080
FRONTEND_PORT=5173

# Spring Boot
SPRING_PROFILES_ACTIVE=dev
LOG_LEVEL=INFO

# Proxy to ChatGPT API (via gateway)
BASE_URL=http://gateway:8080/chatgpt

---

## Project structure

chatsaver/
├── backend/
│ ├── chatsaver-service/ # Chat archiving service
│ ├── eureka-server/ # Eureka registration service
│ ├── config-server/ # Centralized config server
│ ├── gateway/ # API Gateway
│ └── shared-config/ # YAML configuration for Spring Cloud Config
├── frontend/ # Vue 3 web interface for accessing the database
├── docker/
│ ├── compose.yml # Docker Compose file
│ └── postgres/ # Storage and DB initialization
├── .env # Environment variables
├── .gitignore
└── README.md

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

## Переменные окружения (.env)

    # База данных
    POSTGRESQL_HOST=192.168.1.156
    POSTGRESQL_DATABASE=gptchatsaver_db
    POSTGRESQL_USERNAME=user
    POSTGRESQL_PASSWORD=Password123
    POSTGRESQL_PORT=5432

    # Сервисы
    CONFIG_SERVER_URI=http://config-server:8888
    EUREKA_URI=http://eureka-server:8761/eureka
    GATEWAY_PORT=8080
    FRONTEND_PORT=5173

    # Spring Boot
    SPRING_PROFILES_ACTIVE=dev
    LOG_LEVEL=INFO

    # Прокси к API ChatGPT (через gateway)
    BASE_URL=http://gateway:8080/chatgpt

---

## Структура проекта

    chatsaver/
    ├── backend/
    │   ├── chatsaver-service/       # Сервис архивации чатов
    │   ├── eureka-server/           # Сервис регистрации Eureka
    │   ├── config-server/           # Централизованный конфиг-сервер
    │   ├── gateway/                 # API Gateway
    │   └── shared-config/           # YAML конфигурации для Spring Cloud Config
    ├── frontend/                    # Веб-интерфейс на Vue 3 для доступа к БД
    ├── docker/
    │   ├── compose.yml              # Docker Compose файл
    │   └── postgres/                # Хранилище и инициализация БД
    ├── .env                         # Переменные окружения
    ├── .gitignore
    └── README.md

---

