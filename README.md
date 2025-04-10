# Тема 10. Домашня робота

## Опис

У цьому домашньому завданні потрібно доопрацювати REST API-застосунок із
попереднього домашнього завдання.

## Технічний опис завдання

- Реалізуйте механізм аутентифікації в застосунку.
- Реалізуйте механізм авторизації за допомогою **JWT-токенів**, щоб усі операції
  з контактами проводились лише зареєстрованими користувачами.
- Користувач повинен мати доступ лише до своїх операцій з контактами.
- Реалізуйте механізм верифікації електронної пошти зареєстрованого користувача.
- Обмежте кількість запитів до маршруту користувача **/me**.
- Увімкніть **CORS** для свого **REST API**.
- Реалізуйте можливість оновлення аватара користувача (використовуйте сервіс
  **Cloudinary**).

### Основні команди

```bash
        docker compose up
```

```bash
        alembic upgrade up
```

```bash
        fastapi dev main.py
```

### FastAPI

#### auth

```bash
    POST /api/auth/register (User registration)
```

```bash
    POST /api/auth/login (User login)
```

```bash
    GET /api/auth/confirmed_email/{token} (Email confirmation)
```

```bash
    POST /api/auth/request_email (Request email)
```

#### contacts

```bash
    GET /api/contacts/birthdays (Get upcoming birthdays)
```

```bash
    GET /api/contacts/ (Get all contacts)
```

```bash
    POST /api/contacts/ (Create new contact)
```

```bash
    GET /api/contacts/{contact_id} (Get exact contact)
```

```bash
    PUT /api/contacts/{contact_id} (Update exist contact)
```

```bash
    DELETE /api/contacts/{contact_id} (Delete exist contact)
```

#### users

```bash
    GET /api/users/me (requires authentication)
```

```bash
    PATCH /api/users/avatar (Update User avatar)
```

#### healthchecker

```bash
    GET /api/healthchecker (Checking App Health)
```
