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

# Create The Project Directory 📁
```
mkdir Website
```

# Access Your Directory 👉️
```
cd Website
```

## Your Path => [ 📍 ]
```
E:Website
```

# Initialize A Git Repo Within That Directory ⬇️
```
git init
```

# If Starting From An Existing Repo: ⬇️
```
git clone <<repo_url>>
```

# Access Your Directory 👉️
```
cd Website
```

## Your Path => [ 📍 ]
```
E:Website
```

## Create Virtualenv For Your Owner Project 📁
```
python -m venv backend
```


## Access Your Directory 👉️
```
cd backend
```

## Your Path => [ 📍 ]
```
E:Website\backend
```

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

## Create A Requirements File That Contains 📝
## your project dependencies
```
pip freeze > requirements.txt
```

## to install your project requirements 📝
## (if a file already exists)
```
pip install -r requirements.txt
```

## Create A Django Project  => [ ✔️ ]
```
django-admin startproject backend .
```

# Create An App => [ 💻 ]
```
python manage.py startapp pages
```
```
python manage.py startapp product
```

## 🔄 قم بتحديث قاعدة البيانات باستخدام الأمر التالي:
## to update your database for the migrations that
## come with a default django installation
```
python manage.py migrate 
```

# create a superuser to access the admin
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


# Open Settings => [ 📝 ]

> ### The Path [ E:Website\backend\backend\settings.py ]
```

# Import OS 
```
import os
```
