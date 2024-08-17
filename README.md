<div align="center">
    <a href="https://appseed.us/product/adminlte-pro/django/">
        <img src="https://github-production-user-asset-6210df.s3.amazonaws.com/51070104/272178364-cbac6d97-b2dc-4d95-bab6-891f4ee7d84d.png"" width="64" height="64" alt="Rocket Icon">
    </a>
    <h1>
        <a href="https://appseed.us/product/adminlte-pro/django/">
            AdminLTE Django PRO
        </a>
    </h1>
    <p>
        <strong>Bootstrap</strong> &bull; <strong>API (DRF)</strong> &bull; <strong>Celery Beat</strong> &bull; <strong>DataTables</strong> &bull; <strong>Charts</strong> &bull; <strong>Docker</strong> &bull; <strong>CI/CD</strong>
    </p>  
    <h3>
        <a href="https://appseed.us/product/adminlte-pro/django/">
           Download
        </a>
        &nbsp; &bull; &nbsp;        
        <a href="https://django-adminlte-pro.onrender.com">
            Demo
        </a>
        &nbsp; &bull; &nbsp; 
        <a href="https://appseed.us/support/">
            Support
        </a>
    </h3>    
</div>

<br />

<div align="center">
    <img src="https://appsrv1-147a1.kxcdn.com/appseed-v2/media/products/adminlte-pro/top.png" alt="Django AdminLTE PRO - Premium Starter styled with Bootstrap.">
</div>

<br />

## Why [AdminLTE Django PRO](https://appseed.us/product/adminlte-pro/django/)

#### ***Supercharge your app instantly, launch faster, make $***

Login users, process payments and send emails at lightspeed. Spend your time building your startup, not integrating APIs. **AdminLTE Django** provides you with the boilerplate code you need to launch, FAST. 

#### ***Rocket your startup in days, not weeks*** 

The Django boilerplate with all you need to build your SaaS, AI tool, or any other web app. From idea to production in 5 minutes.

#### **48+ hours of headaches**

 - 1 hrs to setup the project 
 - 2 hrs integrate tooling
 - 2 hrs to handle Stripe
 - 1 hrs for Docker
 - 1 hr Google Oauth
 - ∞ hrs overthinking...
 - Free [Support](https://appseed.us/support/) via `Email` & [Discord](https://discord.gg/fZC6hup) 

<br />

## Manual Build 

> 👉 Download code - requires a [purchase](https://appseed.us/product/adminlte-pro/django/) 

```bash
$ unzip django-adminlte-pro.zip
$ cd django-adminlte-pro
```

> 👉 Create `.env` from `env.sample`

```env
DEBUG=False

SECRET_KEY=<STRONG_KEY_HERE>

# For Myql or PgSQL Persistence 
# DB_ENGINE=mysql
# DB_HOST=localhost
# DB_NAME=appseed_django
# DB_USERNAME=root
# DB_PASS=
# DB_PORT=3306
```

> 👉 Install **Django** modules via `VENV`  

```bash
$ virtualenv env
$ source env/bin/activate
$ pip install -r requirements.txt
```

> 👉 Compile React UI

> **Node Version**: `v18.20.0` or above

```bash
$ npm install
$ npm run build
```

> 👉 Migrate DB

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

> 👉 `Create Superuser` & Start the APP

```bash
$ python manage.py createsuperuser # create the admin
$ python manage.py runserver       # start the project
```

<br />

## Start With Docker

> 👉 Download code - requires a [purchase](https://appseed.us/product/adminlte-pro/django/) 

```bash
$ unzip django-adminlte-pro.zip
$ cd django-adminlte-pro
```

> 👉 Start with Docker Compose

```bash
$ docker-compose up --build 
``` 

Visit the app in the browser `localhost:5085`.

<br />

## Use MySql 

By default, the starter uses SQLite for persistence. In order to use MySql, here are the steps: 

- Start the MySql Server
- Create a new DataBase
- Create a new user with full privilegies over the database 
- Install the MySql Python Driver (used by Django to connect)
  - `$ pip install mysqlclient`
- Edit the `.env` with the SQL Driver Information & DB Credentials 

```env

DB_ENGINE=mysql
DB_HOST=localhost
DB_NAME=<DB_NAME_HERE>
DB_USERNAME=<DB_USER_HERE>
DB_PASS=<DB_PASS_HERE>
DB_PORT=3306

```

Once the above settings are done, run the migration & cretae tables: 

```bash
$ python manage.py makemigrations
$ python manage.py migrate
```

<br />

## Production Build

To use the starter in production mode, here are the steps: 

- Set  **DEBUG=False** in `.env`
- Execute `collectstatic` command
  - `$ python manage.py collectstatic --no-input`

As a model, feel free to take a look at [build.sh](./build.sh), the file executed by the CI/CD flow for Render:   


<br />

## **Deploy on Render**

- Create a Blueprint instance
  - Go to https://dashboard.render.com/blueprints this link.
- Click `New Blueprint Instance` button.
- Connect your `repo` which you want to deploy.
- Fill the `Service Group Name` and click on the `Update Existing Resources` button.
- Edit the Environment and [specify the PYTHON_VERSION](https://render.com/docs/python-version)
  - Version `3.12.0` was used for **[this deployment](https://django-adminlte-pro.onrender.com)**
- After that, your deployment will start automatically.

At this point, the product should be LIVE.

<br />

## Codebase 

```bash
< PROJECT ROOT >
   |
   |-- core/                 # Project Settings 
   |    |-- settings.py 
   |    |-- wsgi.py     
   |    |-- urls.py     
   |
   |-- home/                 # Presentation app 
   |    |-- views.py         # serve the HOMEpage  
   |    |-- urls.py     
   |    |-- models.py
   |
   |-- apps/                 # Utility Apps 
   |    |-- common/          # defines models & helpers
   |    |    |-- models.py   
   |    |    |-- util.py 
   |    |-- users            # Handles Authentication 
   |    |-- api              # DRF managed API
   |    |-- charts           # Showcase Different Charts
   |    |-- tables           # Implements DataTables
   |    |-- tasks            # Celery, async processing
   |
   |-- templates/            # UI templates 
   |-- static/               # Tailwind/Flowbite 
   |    |-- src/             # 
   |         |-- input.css   # CSS Styling
   |
   |-- Dockerfile            # Docker
   |-- docker-compose.yml    # Docker 
   |
   |-- render.yml            # CI/CD for Render
   |-- build.sh              # CI/CD for Render 
   |
   |-- manage.py             # Django Entry-Point
   |-- requirements.txt      # dependencies
   |-- .env                  # ENV File
   |
   |-- *************************************************      
```   

<br />

## License

[EULA License](https://github.com/app-generator/license-eula)

<br />

---
[AdminLTE Django PRO](https://appseed.us/product/adminlte-pro/django/) - Premium Seed Project styled with `Bootstrap` actively supported by **[AppSeed](https://appseed.us)**.
