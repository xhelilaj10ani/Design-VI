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
## Starting Django REST Project
I initiated a Django project called "stevens" by running the command:
`django-admin startproject stevens`

Following that, I created a Django app named "myapp" with:
`python manage.py startapp myapp`

Next, I modified the `settings.py` file in `~/mycpu/myvpu`, adding an asterisk to `ALLOWED_HOSTS` and including 'myapp' and 'rest_framework' in `INSTALLED_APPS`. To do this, I used `nano settings.py`.

I then copied the required files:
- I copied `urls.py` to `~/mycpu/mycpu` by running:
  `cp ~/iot/lesson4/mycpu/urls.py .`
  
- Then I copied `admin.py`, `models.py`, `views.py`, and `serializers.py` to `~/mycpu/myapp` with the following commands:
  - `cp ~/iot/lesson4/mycpu/admin.py .`
  - `cp ~/iot/lesson4/mycpu/models.py .`
  - `cp ~/iot/lesson4/mycpu/views.py .`
  - `cp ~/iot/lesson4/mycpu/serializers.py .`

Once these files were copied, I updated the default password 'admin' in `views.py` using `nano views.py`.

Then, I copied `index.html` by executing the following commands:
- `mkdir static templates`
- `cd templates`
- `mkdir myapp`
- `cd myapp`
- `cp ~/iot/lesson4/mycpu/index.html .`

After copying `index.html`, I modified it to add a Google Maps API key using `nano index.html`.

Next, I copied static files by running the following commands in the static directory:
- `cp ~/iot/lesson4/static/*css .`
- `cp ~/iot/lesson4/static/*js .`

I then navigated to the `mycpu` directory and copied `controller.py` with:
`cp ~/iot/lesson4/mycpu/controller.py .`

I also updated the default password 'admin' in `controller.py` by editing the file with `nano controller.py`.

Before running the server, I executed the following commands to ensure the server and database were properly configured:
- `pip3 install -U psutil`
- `python manage.py makemigrations myapp`
- `python manage.py migrate`
- `python manage.py createsuperuser`

Then, I ran the Django server with:
`python manage.py runserver`

I accessed `http://127.0.0.1:8000/admin` and logged in with my Django admin credentials. On the admin panel, I added location data for Stevens. In the HTML form, I submitted:
- `2024` to the DT List at `http://127.0.0.1:8000/dt`
- `20` to the CPU list at `http://127.0.0.1:8000/cpu`
- `20` to the Mem List at `http://127.0.0.1:8000/mem`

After completing these steps, I ran `controller.py` in a separate terminal window with:
`python controller.py`

With the Django server still running, I accessed the app at `http://127.0.0.1:8000/home`.
![run1](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/run1.png)
![run2](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/run2.png)
![run3](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/run3.png)
![runf](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/runf.png)
![apirt](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/apirt.png)
![con.py](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/con.py.png)

The app looked like this:
![cpup](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/cpup.png)

---
## Running Flask Server
To start the Flask server, I navigated to the **lesson4** directory and ran the Python script **hello_world.py** with:
- `cd ~/iot/lesson4`
- `python3 hello_world.py`
![hw1](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/hw1.png)

This is what the server looked like:
![hw2](https://github.com/xhelilaj10ani/Design-VI/blob/main/Labs/Lab%204/hw2.png)

---
## Summary
Through this lab, I gained experience with Django, Django REST framework, and Flask. I learned how to run and access servers, obtain an API key, and perform migrations for manage.py files.
