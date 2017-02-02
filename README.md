#### Site Base URL in Template Context
A simple Django application which add Site base URL to template context processor with each reqeust. You can get Site URL in your template files using `{{ BASE_URL }}`

<br/>
#####Tested Environment
```
Ubuntu 14.04
Python 3.4
Python 2.7
Django 1.10
```

<br/>
#####Installation
<br/>
Using PIP
```
pip install django-baseurl
```

<br/>
Using Source Code (Github)
```
git clone https://github.com/lalzada/django-baseurl.git
```
Switch to `django-baseurl` directory and run command
```
python setup.py install
```

<br/>
Add `django_baseurl` to `INSTALLED_APPS` in `settings.py`
```
INSTALLED_APPS = [
  ...
  
  'django_baseurl'
]
```

<br/>
Add `context processor` to `TEMPLATES` in `settings.py`
```
TEMPLATES = [
    {
        ...
        
        'OPTIONS': {
            'context_processors': [
                ...
                
                'django_baseurl.context_processors.baseurl'
            ],
        },
    },
]
```

<br/>
#####Usage
Use below template variable inside your template file to get Site base url
```
{{ BASE_URL }}
```
