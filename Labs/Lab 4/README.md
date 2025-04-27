# CPE 322 - Lab 4
## Django and Flask
### Dritan Xhelilaj </br>
"I pledge my honor that I have abided by the Stevens Honor System."

---
## Installing Django & Django REST framework
I executed these commands in my terminal to install Django and Django REST framework:
- `pip3 install -U setuptools`
- `pip3 install -U django`
- `pip3 install -U djangorestframework`
- `pip3 install -U django-filter`
- `pip3 install -U markdown`
- `pip3 install -U requests`
![djdwld](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/djdwld.png)

---
## Start Django Project
I started a Django project named "stevens" with the command `django-admin startproject stevens`.
![stevens](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/stevens.png)

After, with the command `python manage.py startapp myapp` I created a Django app called myapp.
![pymyapp](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/pymyapp.png)

Once I launched the app, I ran `python manage.py migrate` to apply the database migrations. This made sure that SQLite was correctly configured for the project.
![pymig](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/pymig.png)

After that, I modified the settings.py file located in ~/stevens/stevens, adding an asterisk ('*') to ALLOWED_HOSTS and including 'myapp' in INSTALLED_APPS. I made these changes using `nano settings.py`.
![set.py](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/set.py.png)

I then copied files from the GitHub lesson4/stevens repository.

1- First, I copied urls.py into ~/stevens/stevens using:
`cp ~/iot/lesson4/stevens/urls.py .`

2- Next, I copied admin.py, models.py, and views.py into ~/stevens/myapp with the following commands:
- `cp ~/iot/lesson4/stevens/admin.py .`
- `cp ~/iot/lesson4/stevens/models.py .`
- `cp ~/iot/lesson4/stevens/views.py .`

3- Finally, I created the necessary directories for templates and copied index.html by running:
- `mkdir static templates`
- `cd templates`
- `mkdir myapp`
- `cd myapp`
- `cp ~/iot/lesson4/stevens/index.html .`
![iot-mkdir](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/iot-mkdir.png)
![mkdir-iot](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/mkdir-iot.png)

After that, I enabled the Google Maps API. I got an API key from the Google Cloud Console and replaced "YOUR_API_KEY" in index.html with my new key. I made this change by editing the file using:
`nano index.html`.
![API_key](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/API_key.png)

Afterward, I copied the static files from the GitHub repository.

1. I first copied favicon.ico using:
- `cp ~/iot/lesson4/static/favicon.ico .`

2. Then I created a *myapp* directory inside static, navigated into it, and copied over the CSS and JavaScript files with:
- `cp ~/iot/lesson4/static/*css .`
- `cp ~/iot/lesson4/static/*js .`
![cp_iot](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/cp_iot.png)

Before starting the server, I ran `python manage.py makemigrations myapp` followed by `python manage.py migrate` to apply the database migrations and make sure everything was up to date.

After that, I launched the Django server using `python manage.py runserver`.
![127.0](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/127.0.png)

While the server was running, I navigated to http://127.0.0.1:8000/admin and logged in using my admin credentials. From there, I added new entries by filling in fields for date/time, temperature, longitude, and latitude, and then saved the data. Afterward, I visited the main Django app at http://127.0.0.1:8000.

The resulting app display is shown below:
![wsp](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/wsp.png)

---
## 
