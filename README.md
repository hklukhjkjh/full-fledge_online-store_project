# Django Online Store

Интернет-магазин на Django с полным циклом покупки: каталог товаров, корзина, оформление заказов и личный кабинет.

## Технологии

- **Backend:** Django 4.2, Python 3.x
- **База данных:** PostgreSQL
- **Изображения:** Pillow
- **Frontend:** Django Templates, CSS

## Функциональные возможности

- **Каталог товаров**
  - Просмотр товаров по категориям
  - Полнотекстовый поиск с ранжированием (PostgreSQL)
  - Детальная страница товара

- **Корзина покупок**
  - Добавление/удаление товаров
  - Изменение количества
  - Подсчёт итоговой суммы

- **Система заказов**
  - Оформление заказа с выбором способа оплаты
  - Валидация номера телефона
  - Управление статусами заказа
  - Автоматическое списание товара со склада

- **Пользователи**
  - Регистрация и вход по email
  - Личный кабинет с историей заказов
  - Редактирование профиля

- **Админ-панель**
  - Управление товарами и категориями
  - Автогенерация slug
  - Отслеживание остатков

## Структура проекта

```
├── core/           # Настройки Django
├── dashboard/      # Каталог и товары
├── users/          # Аутентификация
├── carts/          # Корзина
├── orders/         # Заказы
├── common/         # Общие утилиты
├── templates/      # HTML-шаблоны
└── media/          # Загруженные изображения
```

## Установка

1. Клонируйте репозиторий:
```bash
git clone https://github.com/yourusername/django-online-store.git
cd django-online-store
```

2. Создайте виртуальное окружение и активируйте его:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
```

3. Установите зависимости:
```bash
pip install -r requirements.txt
```

4. Настройте базу данных PostgreSQL в `core/settings.py`:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'your_database_name',
        'USER': 'your_username',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

5. Примените миграции:
```bash
python manage.py migrate
```

6. Создайте суперпользователя:
```bash
python manage.py createsuperuser
```

## Запуск

```bash
python manage.py runserver
```

Откройте в браузере: `http://127.0.0.1:8000/`

Админ-панель: `http://127.0.0.1:8000/admin/`
