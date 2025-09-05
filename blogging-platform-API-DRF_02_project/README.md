
# Blogging Platform API - https://roadmap.sh/projects/blogging-platform-api

RESTful API для персональной блог-платформы на Django и Django REST Framework.  

Позволяет создавать, читать, обновлять и удалять записи блога, категории и теги. Также поддерживается фильтрация постов по поисковому запросу.

---

## 🛠 Технологии

- Python 3.13  
- Django 5.1  
- Django REST Framework  
- DRF Spectacular (Swagger/OpenAPI документация)  

---

## ⚙ Установка

1. Клонируем репозиторий:

```bash
git clone <url>
cd blogging-platform-API-DRF_02_project
````

2. Создаем и активируем виртуальное окружение:

```bash
python -m venv .venv
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows
```

3. Устанавливаем зависимости:

```bash
pip install -r requirements.txt
```

4. Применяем миграции:

```bash
python manage.py migrate
```

5. Загружаем начальные данные (фикстуры):

```bash
python manage.py loaddata post/initial_post.json
```

6. Запускаем сервер:

```bash
python manage.py runserver
```

---

## 🚀 API Endpoints

### Категории

* `GET /categories/` — получить все категории
* `GET /categories/?search=<term>` — поиск категории по названию
* `POST /categories/` — создать категорию
* `PUT/PATCH /categories/<id>/` — обновить категорию
* `DELETE /categories/<id>/` — удалить категорию

### Теги

* `GET /tags/` — получить все теги
* `GET /tags/?search=<term>` — поиск тега по названию
* `POST /tags/` — создать тег
* `PUT/PATCH /tags/<id>/` — обновить тег
* `DELETE /tags/<id>/` — удалить тег

### Посты

* `GET /posts/` — получить все посты
* `GET /posts/?term=<term>` — поиск по заголовку, контенту или категории
* `POST /posts/` — создать новый пост
* `GET /posts/<id>/` — получить пост по ID
* `PUT/PATCH /posts/<id>/` — обновить пост
* `DELETE /posts/<id>/` — удалить пост

---

## 📄 Swagger / OpenAPI

Документация доступна по адресу:

```
http://127.0.0.1:8000/swagger/
```

---

## 📝 Пример данных (фикстуры)

* 4 категории: Technology, Science, Health, Travel
* 5 тегов: Python, Django, AI, HealthTips, TravelGuide
* 5 постов с привязкой к категориям и тегам

---

