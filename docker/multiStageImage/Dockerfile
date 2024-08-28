# Этап 1: Сборка приложения
FROM golang:1.20-alpine as builder

# Установка зависимостей
RUN apk add --no-cache git

# Создание директории для кода
WORKDIR /app

# Копирование файлов проекта в контейнер
COPY . .

# Сборка приложения
RUN go build -o myapp .

# Этап 2: Создание финального образа
FROM alpine:3.18

# Установка только необходимых зависимостей
RUN apk add --no-cache ca-certificates

# Копирование приложения из предыдущего этапа
COPY --from=builder /app/myapp /usr/local/bin/myapp

# Определение команды для запуска контейнера
CMD ["myapp"]
