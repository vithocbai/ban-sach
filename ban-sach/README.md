# 📚 Book Store

Website bán sách online với:

* ReactJS + Vite
* Tailwind CSS
* Django REST Framework
* PostgreSQL
* JWT Authentication

## Requirements

* Node.js
* Python 3.11+
* PostgreSQL

## Setup

### Backend

```bash
cd backend

python -m venv venv
venv\Scripts\activate       # Windows
# source venv/bin/activate  # macOS/Linux

pip install -r requirements.txt

python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Backend:

```text
http://127.0.0.1:8000
```

### Frontend

```bash
cd frontend

npm install
npm run dev
```

Frontend:

```text
http://localhost:5173
```

## Environment

### Backend `.env`

```env
DEBUG=True
SECRET_KEY=your-secret-key

DATABASE_NAME=bookstore
DATABASE_USER=postgres
DATABASE_PASSWORD=your-password
DATABASE_HOST=localhost
DATABASE_PORT=5432
```

### Frontend `.env`

```env
VITE_API_URL=http://127.0.0.1:8000/api
```

## Structure

```text
book-store/
├── frontend/
├── backend/
├── PROJECT_PLAN.md
├── DESIGN_SYSTEM.md
└── README.md
```

## Admin

```text
http://127.0.0.1:8000/admin/
```

## Documentation

* `PROJECT_PLAN.md` — Project architecture & features
* `DESIGN_SYSTEM.md` — UI/UX design system
