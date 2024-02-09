<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------------------------------->
<!------- Abdelrahman Gamal ----->
<!------------- [ 1 ] ----------->


# 0️⃣ [ Open Commend ]

## Pytho Version
```
python --version 
```

## Pip Version
```
pip --version
```

## Install Virtualenv Globally 📦
```
pip install virtualenv
```

## Create The Project Directory 📁
```
mkdir Website
```

# Access Your Directory 👉️
```
cd Website
```
> ## Your Path => [ 📍 ] E:Website

## Create Virtualenv For Your Owner Project 📁
```
python -m venv backend
```

## Access Your Directory 👉️
```
cd backend
```

> ### Your Path => [ 📍 ] E:Website\backend

## Activate Your Virtualenv  => [ ✔️ ]
```
Scripts\activate
```

## Install Django => [ 📦 ]
```
pip install django
```

## Upgrade Django ( If Necessary ) => [ 📦 ]
```
pip install -U Django
```

## Upgrade Pip ( If Necessary ) => [ 📦 ]
```
py -m pip install --upgrade pip
```

## Create A Django Project  => [ ✔️ ]
```
django-admin startproject backend .
```

## Create An App => [ 💻 ]
```
python manage.py startapp pages
```
```
python manage.py startapp products
```

## 🔄 قم بتحديث قاعدة البيانات باستخدام الأمر التالي:
## to update your database for the migrations that
## come with a default django installation
```
python manage.py migrate
```

## create a superuser to access the admin
```
python manage.py createsuperuser
```

## Run Server => [ 💻 ]
```
python manage.py runserver
```
```
python manage.py runserver 8001
```
```
python manage.py runserver 0.0.0.0:8000
```
## [ Go To  ] 👉️
```
http://127.0.0.1:8000/
```

## [ Go To  ] 👉️
```
http://127.0.0.1:8000/admin/
```
_______________________________________

## Edit Settings.py  In Project => [ 📝 ]
> ##### Your Path [ E:Website\backend\backend\settings.py ]

## Add Your App To INSTALLED_APPS => [ 💻 ]
```
INSTALLED_APPS = [
    'pages.apps.PagesConfig',
    'products.apps.ProductsConfig',
    # . . .
]
```
_______________________________________
## Edit Urls.py In Project => [ 📝 ]
> ##### Your Path [ E:Website\backend\backend\urls.py ]
```
from django.contrib import admin
from django.urls import path
from django.urls import include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('pages.urls')),
    path('', include('products.urls')),
]
```
_______________________________________
## [ Create File urls.py In Side App ] => [ 📝 ]

> ##### Your Path => E:Website\backend\backend\pages
> ##### Your Path => E:Website\backend\backend\Products
```
urls.py
```

## [ Add This Code In Pages App And Products App ] => [ 📝 ]
```
from django.urls import path
from . import views
urlpatterns = [
  path('', views.index, name='index'),
]
```
```
from django.urls import path
from . import views
urlpatterns = [
  path('products', views.products, name='products'),
  path('product', views.product, name='product'),
]
```
_______________________________________
## [ Views File In Side App  ] => [ 📝 ]
#### [ 1 ]
```
from django.http import HttpResponse
Create your views here.
def index(request):
  return HttpResponse("Hello, world. You're at the index page.")
```
#### [ 2 ]
```
from django.shortcuts import render
def index(request):
  return render(request, 'pages/index.html')
```
#### [ 3 ] Data In Templates
```
from django.shortcuts import render
def index(request):
  return render(request, 'pages/index.html', {'name': 'Hossam Rashad'})
```

#### [ 4 ] Data In Templates
```
from django.shortcuts import render
def index(request):
  return render(request, 'pages/index.html', {'name': 'Hossam Rashad', 'age': 30})
```

#### [ 5 ]  Data In Templates
```
from django.shortcuts import render
def index(request):
  x = {'name': 'Hossam Rashad', 'age': 20}
  return render(request, 'pages/index.html', x)
```
#### [ 6 ] Felters In Templates With Data
```
from django.shortcuts import render
def index(request):
  x = {
    "empty": "",
    "name": "Hossam Rashad",
    "title": "Home Page",
    "age": 20,
    "list": [1, 2, 3],
    "dict": {"a": 1, "b": 2},
    "none": None,
    "bool": True,
    "bool2": False,
    "fileSize":16154544889,
    "fileSize1":54645758,
    "fileSize2":111000,
    "fileSize3":503
  }
  return render(request, 'pages/index.html', x)
```
_______________________________________
## [ Create Templates Folder  ] => [ 📁 ]

E:Website\backend\backend\

```
📁 backend
📁 pages
📁 products
📁 templates
  📁 pages
  └── 📝 index.html
  📁 products
  └── 📝 products.html
  └── 📝 product.html

templates
  pages
    index.html

templates\pages\index.html
```
#### [ 2 ]
```
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h1>Hello World!</h1>
    <h2>Home Page</h2>
    <p>Welcome to my first Django project!</p>
  </body>
</html>
```
#### [ 3 ] Data In Templates
```
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h2>Name = {{name}}</h2>
  </body>
</html>
```

#### [ 4 ] Data In Templates
```
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h2>Name = {{name}}</h2>
    <h2>Age = {{age}}</h2>
  </body>
</html>
```
#### [ 5 ]  Data In Templates
```
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h2>Name = {{name}}</h2>
    <h2>Age = {{age}}</h2>
  </body>
</html>
```
#### [ 6 ] Felters In Templates With Data
```
<!DOCTYPE html>
<html>
  <head>
  </head>
  <body>
    <h2>If No Data = {{empty|default:"Nothing Found"}}</h2>
    <h2>String Slice = {{title|slice:5}}</h2>
    <h2>String Slice = {{title|slice:'0:5'}}</h2>
    <h2>Add String Or Value = {{title|add:" Index"}}</h2>
    <h2>Add String Or Value = {{title|add:" Index"}}</h2>
    <h2>String Length = {{title|length}}</h2>
    <h2>String Cut = {{title|cut:' '}}</h2>
    <h2>String Cut = {{title|cut:'o'}}</h2>
    <h2>String To Lower Case = {{title|lower}}</h2>
    <h2>String First To Upper Case = {{title|capfirst}}</h2>
    <h2>String To Upper Case = {{title|upper}}</h2>
    <h2>age = {{age}}</h2>
    <h2>File Size = {{fileSize|filesizeformat}}</h2>
    <h2>File Size = {{fileSize1|filesizeformat}}</h2>
    <h2>File Size = {{fileSize2|filesizeformat}}</h2>
    <h2>File Size = {{fileSize3|filesizeformat}}</h2>
  </body>
</html>
```
#### [ Tag In DTL ]
- Extends 
#### [ 1 ]
```
Page Base
<style>
  body {
    background: #000
  }
</style>
```
```
Page Index
{% extends 'base/base.html' %}
```
#### [ 2 ]
#### [ 3 ]
#### [ 4 ]
#### [ 5 ]
- Extends 
- Block 
- Include
- If
- For
- Url



_______________________________________

## Edit Settings.py  => [ 📝 ]
> ##### Your Path [ E:Website\backend\backend\settings.py ]

# Import OS L => [ 📦 ]
```
import os
```

## Add TEMPLATES => [ 💻 ]
```
TEMPLATES = [
  {
    'DIRS': [os.path.join(BASE_DIR, 'templates')],
    # ...
  },
]
```
