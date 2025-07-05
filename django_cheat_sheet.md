
# Django Cheat Sheet 

## SECRET_KEY
- It's a random string used by Django for:
  - Password hashing
  - CSRF protection
  - Session encryption
- Keep it secret in production (use `.env` files or environment variables).

---

## Default Django Apps in `INSTALLED_APPS`
```python
'django.contrib.admin',
'django.contrib.auth',
'django.contrib.contenttypes',
'django.contrib.sessions',
'django.contrib.messages',
'django.contrib.staticfiles',
````

* These are built-in apps.
* You can add your own apps like `'videos'`.

---

## Middleware

Middleware is like a filter that processes requests/responses.
They run **before and after** views.

### Common Middleware:

* `SecurityMiddleware`: Adds security headers
* `SessionMiddleware`: Handles user sessions
* `CommonMiddleware`: Adds headers for redirects etc.
* `CsrfViewMiddleware`: Protects against CSRF attacks
* `AuthenticationMiddleware`: Associates users with requests
* `MessageMiddleware`: Sends messages to users
* `XFrameOptionsMiddleware`: Protects against clickjacking

---

## Django Security

### CSRF (Cross-Site Request Forgery)

* Prevents unauthorized POST requests from other sites.
* Use `{% csrf_token %}` in HTML forms.

### XSS (Cross-Site Scripting)

* Attacker injects JavaScript in pages.
* Django auto escapes data using `{{ data }}` safely.

### Clickjacking

* Attacker tricks users into clicking hidden UI.
* Use `X-Frame-Options: DENY` (enabled via middleware).

---

## WSGI (Web Server Gateway Interface)

* A standard interface between web servers (e.g., Gunicorn) and Python apps.
* Django apps are WSGI-compatible via `wsgi.py`.

---

## Models

### `on_delete=models.CASCADE`

* If a parent model is deleted, child model also gets deleted.
* Used in ForeignKey.

### Common Fields

* `CharField`, `TextField`, `IntegerField`, `FloatField`
* `DateTimeField`, `ImageField`, `FileField`, `BooleanField`

### Validators

* `MinValueValidator`, `MaxLengthValidator`, etc.
* You can create custom validators too.

---

## Python Module vs Python Class

* **Module**: A `.py` file (e.g., `models.py`)
* **Class**: Defined inside modules (e.g., `class Video(models.Model)`)

---

## Django ORM (Object Relational Mapping)

Use Python code to interact with database.

### Django Shell

```bash
python manage.py shell
```

### Example Queries

```python
from videos.models import Video

Video.objects.all()
Video.objects.filter(title="Demo")
Video.objects.get(id=1)
```

### ORM to SQL

```python
print(Video.objects.filter(id=1).query)
```

---

## Aggregations & Annotations

* **Aggregation**: Get a single value like count or sum.

```python
from django.db.models import Count
Video.objects.aggregate(Count('id'))
```

* **Annotation**: Add calculated fields to querysets.

```python
Video.objects.annotate(num_comments=Count('comment'))
```

---

## Migration Files

* Auto-generated when you create or change models.
* Stores schema changes.

```bash
python manage.py makemigrations
python manage.py migrate
```

---

## SQL Transactions

* A transaction is a group of SQL operations that succeed or fail together.
* Ensures data consistency.
* Begin → Do multiple things → Commit or Rollback

---

## Atomic Transactions

* Ensures all DB operations inside a block happen or none happen.

```python
from django.db import transaction

with transaction.atomic():
    # Your DB operations here
```

---

## Useful Django Commands

```bash
django-admin startproject myproject
python manage.py startapp myapp
python manage.py runserver
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
```

---

## Tips

* Use Django Admin for quick backend.
* Use `MEDIA_URL` and `MEDIA_ROOT` for file uploads.
* Always test forms with CSRF tokens.
