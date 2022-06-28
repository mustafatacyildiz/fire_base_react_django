React'i djangoya bağlamak için;

pip install django-cors-headers

setting.py
ALLOWED_HOSTS = ['*']
INSTALLED_APPS = [
  # ...
  'corsheaders',
]
MIDDLEWARE = [
  # ...
  'django.contrib.sessions.middleware.SessionMiddleware',
  'corsheaders.middleware.CorsMiddleware',
  'django.middleware.common.CommonMiddleware',
  # ...
]
CORS_ORIGIN_ALLOW_ALL = True
CORS_ALLOW_CREDENTIALS = True
CORS_EXPOSE_HEADERS = (
  'Access-Control-Allow-Origin: *',
)