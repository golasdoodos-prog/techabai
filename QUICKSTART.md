# Быстрый старт

## Вариант 1: С Docker (рекомендуется)

### 1. Запуск MongoDB
```bash
# Запуск MongoDB и Mongo Express
docker-compose up -d

# Проверка статуса
docker-compose ps
```

### 2. Установка зависимостей
```bash
# Установка зависимостей сервера
npm install

# Установка зависимостей клиента
cd client
npm install
cd ..
```

### 3. Настройка окружения
Создайте файл `.env` в корневой папке:
```env
MONGODB_URI=mongodb://admin:password@localhost:27017/tech-support?authSource=admin
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
PORT=5000
```

### 4. Инициализация базы данных
```bash
npm run init-db
```

### 5. Запуск приложения
```bash
# Терминал 1: Сервер
npm run dev

# Терминал 2: Клиент
cd client
npm start
```

## Вариант 2: Локальная MongoDB

### 1. Установка MongoDB
- Скачайте и установите MongoDB Community Server
- Запустите MongoDB сервис

### 2. Настройка окружения
Создайте файл `.env`:
```env
MONGODB_URI=mongodb://localhost:27017/tech-support
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production
PORT=5000
```

### 3. Остальные шаги
Следуйте шагам 2-5 из Варианта 1.

## Доступ к приложению

- **Веб-приложение**: http://localhost:3000
- **API сервер**: http://localhost:5000
- **Mongo Express** (если используете Docker): http://localhost:8081

## Администратор по умолчанию

После инициализации базы данных будет создан администратор по умолчанию:

### Администратор
- **Email:** `admin@example.com`
- **Пароль:** `admin123`

С помощью этого аккаунта вы можете:
- Создавать новых пользователей
- Создавать новых администраторов
- Управлять всеми заявками в системе

## Остановка

### Docker
```bash
docker-compose down
```

### Локальная MongoDB
Остановите MongoDB сервис через системные службы.

## Возможные проблемы

### Порт 27017 занят
```bash
# Проверка процессов на порту
netstat -ano | findstr :27017

# Остановка процесса (Windows)
taskkill /PID <PID> /F
```

### Ошибка подключения к MongoDB
- Убедитесь, что MongoDB запущен
- Проверьте строку подключения в `.env`
- Для Docker: убедитесь, что контейнер запущен (`docker-compose ps`)

### Ошибки при установке зависимостей
```bash
# Очистка кэша npm
npm cache clean --force

# Удаление node_modules и переустановка
rm -rf node_modules package-lock.json
npm install
```
