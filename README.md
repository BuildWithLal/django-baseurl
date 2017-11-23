#### Site Base URL in Template Context
A simple Django application which add Site base URL (with port if used any) to template context processor with each reqeust. You can get Site URL in your template files using `{{ BASE_URL }}`

<br/>

##### Tested Environment
```
Ubuntu 14.04
Python 3.4
Python 2.7
Django 1.10
```

<br/>

##### Installation
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

Add `django_baseurl` to `INSTALLED_APPS` in `settings.py`. 

<br/>

```
INSTALLED_APPS = [
  ...
  
  'django_baseurl'
]
```

<br/>

Add `context processor` to `TEMPLATES` in `settings.py`

<br/>

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

#### Usage
Use below template variable inside your template file to get Site base url (with port if used any)

```
{{ BASE_URL }}
```

<br/>
This package can be found on PyPi [here](https://pypi.python.org/pypi/django_baseurl)
