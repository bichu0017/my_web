# Portfolio Project – File Structure

```
portfolio_project/
├── config/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
├── portfolio/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── services.py          ← Supabase helpers
│   ├── urls.py
│   ├── views.py
│   ├── static/
│   │   ├── css/portfolio.css
│   │   └── js/portfolio.js
│   └── templates/portfolio/
│       ├── base.html
│       ├── index.html       ← public portfolio page
│       ├── dashboard.html   ← admin/owner dashboard
│       └── login.html       ← admin login page
├── templates/
│   └── registration/
│       └── login.html
├── .env                     ← SUPABASE_URL + SUPABASE_KEY + SECRET_KEY
├── manage.py
└── requirements.txt
```

## Setup

```bash
pip install -r requirements.txt
cp .env.example .env   # fill in your Supabase credentials
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

## Pages
| URL | Description |
|-----|-------------|
| `/` | Public portfolio (read-only) |
| `/dashboard/` | Admin dashboard – add/edit/delete projects & images, edit profile |
| `/admin/` | Django admin panel |
| `/accounts/login/` | Login page |
