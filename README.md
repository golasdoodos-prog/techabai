# 🛠️ Tech Support Site

Сайт технического обслуживания с системой заявок для управления техническими проблемами.

## ✨ Возможности

- 👥 **Управление пользователями** - создание пользователей и администраторов
- 🎫 **Система заявок** - создание, отслеживание и управление заявками
- 🔐 **Безопасность** - JWT аутентификация, сброс паролей
- 📊 **Отчеты** - генерация PDF отчетов для администраторов
- 🔔 **Уведомления** - отслеживание изменений статуса заявок
- 📱 **Адаптивный дизайн** - работает на всех устройствах

## 🚀 Быстрый старт

### Требования
- Node.js 16+
- MongoDB
- npm или yarn

### Установка

1. **Клонируйте репозиторий:**
```bash
git clone https://github.com/ВАШ_ПОЛЬЗОВАТЕЛЬ/tech-support-site.git
cd tech-support-site
```

2. **Установите зависимости:**
```bash
npm install
cd client
npm install
cd ..
```

3. **Настройте переменные окружения:**
```bash
# Создайте файл .env в корне проекта
MONGODB_URI=mongodb://localhost:27017/tech-support
JWT_SECRET=your-super-secret-jwt-key-here
PORT=5000
NODE_ENV=development
```

4. **Инициализируйте базу данных:**
```bash
npm run init-db
```

5. **Запустите сервер:**
```bash
npm run dev
```

6. **Запустите клиент (в новом терминале):**
```bash
cd client
npm start
```

## 🔑 Доступ по умолчанию

- **URL:** http://localhost:3000
- **Админ логин:** `admin`
- **Админ пароль:** `admin123`

## 🛠️ Технологии

### Backend
- Node.js + Express
- MongoDB + Mongoose
- JWT аутентификация
- Puppeteer (PDF генерация)

### Frontend
- React 18
- React Router
- React Hook Form
- Lucide React (иконки)
- Tailwind CSS

## 📁 Структура проекта

```
tech-support-site/
├── client/                 # React приложение
│   ├── public/
│   ├── src/
│   │   ├── components/     # React компоненты
│   │   ├── pages/         # Страницы
│   │   ├── contexts/      # React контексты
│   │   └── App.js
│   └── package.json
├── models/                # Mongoose модели
├── routes/               # API маршруты
├── middleware/           # Express middleware
├── scripts/             # Скрипты инициализации
├── server.js           # Главный файл сервера
└── package.json
```

## 🔧 API Endpoints

### Аутентификация
- `POST /api/auth/login` - Вход в систему
- `GET /api/auth/me` - Получение информации о пользователе
- `PATCH /api/auth/change-password` - Изменение пароля

### Заявки
- `GET /api/tickets/my` - Мои заявки
- `POST /api/tickets` - Создание заявки
- `GET /api/tickets/:id` - Получение заявки

### Админ
- `GET /api/admin/tickets` - Все заявки
- `PATCH /api/admin/tickets/:id/status` - Изменение статуса
- `GET /api/admin/users` - Все пользователи
- `POST /api/admin/users` - Создание пользователя
- `PATCH /api/admin/users/:id/reset-password` - Сброс пароля

## 🚀 Развертывание

### Vercel (рекомендуется)
1. Подключите репозиторий к Vercel
2. Настройте переменные окружения
3. Используйте MongoDB Atlas для базы данных

### Heroku
1. Создайте приложение в Heroku
2. Подключите GitHub репозиторий
3. Настройте переменные окружения
4. Используйте MongoDB Atlas

## 📝 Лицензия

MIT License

## 👥 Авторы

Tech Support Team

---

**Создано с ❤️ для управления техническим обслуживанием**