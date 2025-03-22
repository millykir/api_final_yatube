# Yatube API
Приложение в виде социальной сети, включающее возможность для пользователей делиться постами, комментировать их, вступать в группы и подписываться на других участников.

## Как запустить проект:

1. Создайте виртуальное окружение и активируйте его:

```bash
python3 -m venv .venv
```

Для активации окружения:

```bash
source .venv/bin/activate
```

2. Установка всех зависимостей:

Обновите pip:

```bash
python -m pip install --upgrade pip
```

И установите зависимости из `requirements.txt`:

```bash
pip install -r requirements.txt
```

3. Примените миграции:

```bash
python manage.py migrate
```

4. Для запуска проекта используйте команду:

```bash
python manage.py runserver
```

## Примеры API-запросов:
Полный список доступных запросов доступен в документации по ссылке `/redoc/`.

- **Добавление нового поста**:

```http
POST /api/v1/posts/
{
    "text": "string"
}
```

- **Получение постов с пагинацией**:

```http
GET /api/v1/posts/?limit=10&offset=10
```

- **Получение комментариев для поста**:

```http
GET /api/v1/posts/{post_id}/comments/
```

- **Удаление комментария**:

```http
DEL /api/v1/posts/{post_id}/comments/{comment_id}/
```
