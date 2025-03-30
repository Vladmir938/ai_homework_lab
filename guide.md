# Как выгрузить Django-проект с GitHub через консоль

## 1. Клонируйте репозиторий
Если у вас ещё нет проекта локально, скачайте его с GitHub:
```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```
Перейдите в папку проекта:
```bash
cd REPOSITORY
```

---

## 2. Создайте и активируйте виртуальное окружение
```bash
python -m venv venv
source venv/bin/activate  # Для Linux/Mac
venv\Scripts\activate  # Для Windows
```

---

## 3. Установите зависимости
```bash
pip install -r requirements.txt
```

---

## 4. Настройте переменные окружения
Создайте файл `.env` и добавьте в него необходимые настройки (например, `SECRET_KEY`, параметры базы данных и другие конфигурации).

---

## 5. Примените миграции базы данных
```bash
python manage.py migrate
```

---

## 6. Создайте суперпользователя (если нужно)
```bash
python manage.py createsuperuser
```

---

## 7. Запустите сервер разработки
```bash
python manage.py runserver
```
Теперь проект доступен по адресу `http://127.0.0.1:8000/`.

---

## 8. Как получить обновления из удалённого репозитория
Если проект уже скачан, но в репозитории появились новые изменения, выполните:
```bash
git pull origin main
```

