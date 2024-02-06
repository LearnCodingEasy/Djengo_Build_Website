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

## [ Go To  ] 👉️
```
http://127.0.0.1:8000/
```

## [ Go To  ] 👉️
```
http://127.0.0.1:8000/admin/
```
_______________________________________
_______________________________________
_______________________________________
_______________________________________
_______________________________________

## Edit Settings.py  => [ 📝 ]
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
_______________________________________
_______________________________________
_______________________________________
_______________________________________
## Edit Urls.py => [ 📝 ]
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
_______________________________________
_______________________________________
_______________________________________
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
_______________________________________
_______________________________________
_______________________________________
_______________________________________
## [ Views File In Side App  ] => [ 📝 ]
_______________________________________
_______________________________________
_______________________________________
_______________________________________
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

_______________________________________
_______________________________________
_______________________________________
_______________________________________
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
