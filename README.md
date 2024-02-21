<h1>Django CRM with mySQL: Follow along project.</h1>

<p>This is a simple a Django project that builds a CRM. It is a follow along project that you can also build yourself: https://youtu.be/t10QcFx7d5k?si=dguLHTExW12x4P3E </p>

<h2>What is this project for and what to expect?</h2>

<p>This project is perfect if you are a beginner in Django. It will mainly require you some basic Python. I highly encourage however to read the official Django documentation: https://docs.djangoproject.com/en/5.0/</p>

<p>In this project you can expect:</p>
<ul>
<li>Python code (OOP and scripts)</li>
<li>Administrative tasks on Django</li>
<li>How to download and use mySQL for this specific project</li>
<li>Build the most basic CRM</li>
</ul>

<h2>Getting Started</h2>

<h3>Clone this project</h3>

<p>If you don't want to following along the project on Youtube, you could always clone this project and make it run directly to see the end result. 
However, I do encourage anyone trying to learn Python, especially Django, to try to reproduce this project.</p>

```
git clone https://github.com/kevinbuilds/Django_CRM_mySQL.git
```

<h3>Install MySQL</h3>

<p>In order for this project to work properly, you need to install MYSQL on your computer. <br/>
You can choose between downloading it directly from the official website: https://dev.mysql.com/downloads/mysql/. </br>However, this is not the only way to download MySQL. You could use Brew if you are on a MAC.
</p>

<h4>Downloading MySQL using Brew</h4>
<p>This applies if you are on MAC. In this project we used the latest possible version of mySQL. Here are the steps you need to follow.</p>

<p> Go to your terminal and execute the following command:</p>

```
brew install mysql #This will install mysql
brew servies start mysql #This will launch mysql
mysql_secure_installation #This will secure installation command to setup root password
```

<p>One additional tool you could download to make this project work is mysql work bench that you can find by following this link: https://www.mysql.com/products/workbench/.</p>


<h3>Install all the required packages</h3>

<p>There are many packages, including Django that you need to install. To insure this project works, I would recommend you use all the version in the actual requirements.txt.</p>

```
pip3 install -r requirements.txt
```

<p>You could always download individually all the different packages but I wouldn't recommend it.</p>

<h3>Launch the project</h3>

<h4>Making sure your database works</h4>

<p>You will first need to change some details in the settings.py file in the dcrm folder by making sure you add the right password for your mysql database. I used the default port, but make the required changes if necessary.</p>

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'elderco',
        'USER': 'root',
        'PASSWORD': 'ADD YOUR PASSWORD HERE',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
```

<p>Then you will have to make a migration of your model to mysql. Normally, the file is already here. Launch the following command:</p>

```
python manage.py migrate
```

<p>In case this doesn't work yet, you can always make a migration first.</p>

```
python manage.py makemigrations
python manage.py migrate
```

<h4>Launch the project</h4>

<p>Once you have done all this steps, you should be good to launch your project:</p>

```
python manage.py runserver
```

<h2>Precision about the project</h2>

<h3>Structure of the project</h3>

<p>This project is a Django Project. In case you want to know more about Django, I'd recommend taking a course. In case you don't want to, here are some key indications.</p>

<h4>The different parts</h4>

<p>This project is divided and subdivided as following:</p>

<ul>
<li>There are two main folder: dcrm and website,</li>
<li>dcrm contains settings and urls at Django level,</li>
<li>website contains all settings concerning the application,</li>
<li>manage.py is the file that will run your app,</li>
<li>./DjangoCRMmySQL/website/templates contains all the HTML files,</li>
<li>./DjangoCRMmySQL/website/urls contains all the urls of your app.</li>
</ul>

<h4>Styling the project</h4>

<p>This project uses the latest version of Bootstrap: https://getbootstrap.com/docs/5.3/getting-started/introduction/. </p>

