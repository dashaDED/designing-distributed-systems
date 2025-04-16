# Используем официальный образ Node.js
FROM node:14

# Устанавливаем рабочую директорию
WORKDIR /usr/src/app

# Копируем package.json и устанавливаем зависимости
COPY package*.json ./
RUN npm install

# Копируем остальные файлы приложения
COPY . .

# Устанавливаем переменную окружения для пути к медиафайлам
ENV MEDIA_PATH=/usr/src/app/media

# Открываем порт
EXPOSE 8080

# Запускаем сервер
CMD ["node", "server.js"]
