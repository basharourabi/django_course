# Docker Ancaconda (Docker) Course - Module 2
This is my Docker course. I hope you like it.

> These notes follow on from the README.md getting started instructions.
***
***

## Docker Conda                                          Docker تشغيل أناكوندا بداخل   ##
To download Docker with anaconda image               حمل صورة لنظام دوكر يشمل أناكوندا 

Steps/Commands
You should now have a directory called 'drf_course' in your development directory. This will be known as your 'root directory'.


Docker is an open platform for developers and system administrators to build, ship, and run distributed applications, whether on laptops, data center virtual machines, or the cloud. Anaconda, Inc. provides Anaconda and Miniconda Docker images.

Read the official Docker documentation and specifically the information related to Docker images.

Begin by browsing the available Anaconda images on our Docker profile.

To obtain a fully working Anaconda image:

In a terminal window, run this command to display a list of available images:

docker search continuumio
Pull the desired image:
```
docker pull continuumio/miniconda3
```
Create a container using the image:
```
docker run -t -i continuumio/miniconda3 /bin/bash
```
This gives you direct access to the container where the conda tool is already available.

Test the container:

```
conda info
```
You now have a fully working Anaconda image.


In this module, we will be start our project. To do this we will need to create a virtual environment.
>Note: Python virtual env docs can be found

1) Initiate an account with Docker.com     
-Goto
```
https://Docker.com
```
2) Download Docker Desktop     سطح العمل Docker Desktop إنزال وتحميل
Full Documentation on Docker Desktop & Download Link

-Goto
```
https://docs.docker.com/desktop/install/windows-install/
```
> These notes follow on from the README.md getting started instructions.
***
***

## Docker for Desktop                                                  سطح العمل ل Docker ##
To download Docker for Desktop
 Steps/Commands
You should now have a directory called 'drf_course' in your development directory. This will be known as your 'root directory'.

In this module, we will be start our project. To do this we will need to create a virtual environment.
>Note: Python virtual env docs can be found

1) Initiate an account with Oracle.com     
-Goto
```
https://Docker.com
```
2) Download mySQL WorkBench      سطح العمل MYSQL إنزال وتحميل
-Goto
```
https://github.com/datacharmer/test_db
```

3) Download mySQL WorkBench      سطح العمل MYSQL إنزال وتحميل
-Goto

> These notes follow on from the README.md getting started instructions.
```
https://github.com/datacharmer/test_db
```


## Docker for Desktop                                                  سطح العمل ل Docker ##
To download Docker for Desktop
 Steps/Commands
You should now have a directory called 'drf_course' in your development directory. This will be known as your 'root directory'.

In this module, we will be start our project. To do this we will need to create a virtual environment.
>Note: Python virtual env docs can be found

1) Initiate an account with Docker.com     
-Goto
```
https://Docker.com
```
2) Download mySQL WorkBench      سطح العمل MYSQL إنزال وتحميل
-Goto
```
(https://hub.docker.com/r/genschsa/mysql-employees)
```
3) After Download Proceed with installation      MYSQLworkbench  حمل بعد الإنزال

4) Start A Database Connection     إبدأ الإتصال بعد الإنزال
![Alt text](https://github.com/basharourabi/django_course/blob/main/static_files/MySQLWorkbench_zqUHOFlbG8.png)


5) Enter Database Credentials & Settings for Database Connection       أدخل إعدادات الإتصال ونعريف المستخدم 
   ![Alt text](https://github.com/basharourabi/django_course/blob/main/static_files/ShareX_0CJwYMSi4V.png)



## Steps/Commands
You should now have a directory called 'drf_course' in your development directory. This will be known as your 'root directory'.

In this module, we will be start our project. To do this we will need to create a virtual environment.
>Note: Python virtual env docs can be found [here](https://docs.python.org/3/tutorial/venv.html).

1) Virtual Environment      ألبيئة الإفتراضية
- Open a terminal and use the following command to create a virtual environment. 
```
python -m venv venv
```
Now activate the virtual environment with the following command. تفعيل البيئة الإفتراضية
```
# windows machine
venv\Scripts\activate.bat

#mac/linux
source venv/bin/activate
```
You will know your virtual environment is active when your terminal displays the following:
سوف تعلم أن تفعيل البيئة الإفتراضية مفعلة لأن إسم البيئة بين قوسين على بداية سطر الأمر
```
(venv) path\to\project\drf_course>
```

2) Packages and requirements - Our project will rely on a whole bunch of 3rd party packages (requirements) to function. We will be using a Python package manager to install packages throughout this course. 
I have already created a requirements.txt file. Check out /backend/requirements.txt

 
 backend ووضعه بمجلد   (requirements.txt) لبرمجة البيئة الإفتراضية عليك إنشاء ملف يإسم
يجب الإلتزام برقم الإصدارات حيث تغيير إرتباط الإصدارات قد ىؤدي الى مشاكل  
```
asgiref==3.5.2
Django==4.1.3
django-extensions==3.2.1
django-filter==22.1
djangorestframework==3.14.0
djangorestframework-jsonapi==6.0.0
inflection==0.5.1
python-dotenv==0.21.0
pytz==2022.6
sqlparse==0.4.3
tzdata==2022.6
```
Let's go ahead and install our project requirements. Add the following code to you terminal.
لتفعيل البيئة الإفتراضية عليك  تثبيت ملف يإسم (requirements.txt) وتحديد موقعه من خلال تحديد اسم المجلد اللذي يحتويه


```
pip install -r backend/requirements.txt
```

3) Django - You can now go ahead and start a new Django project. Installing Django has given you access to a handy 'startproject' command. Use the following command to start our new project.
لتفعيل وتثلبيت مشروع منصة django عليك التثبيت من خلال الأوامر التالية 
```
django-admin startproject drf_course backend
```

4) Secrets and Environment Variables - It is good practice to separate sensitive information from your project. We have installed a package called 'python-dotenv' that helps us manage secrets easily. Lets go ahead and create a env file to store information that is specific to our working environment. Use the following command in your terminal.

المصطلحات والكلمات السرية المستخدمة يجب أن تفصل عن باقي ملفات المشروع، وعليه سوف ننشئ بيئة  إفتراضية  جديدة من الممكن فصلها لاحقا وتسمية هذه البيئة env. 

```
# windows machine
copy env.template .env

#mac/linux
cp env.template .env
```

You can use your new .env file to store API keys, secret_keys, app_passwords and you will gain access to these in the Django app.
***
***

## New Root directory
>Note: If all went well, your root directory should now look like this
إذا مشي كل شيئ علا ما يرام سوف يكون شكل تكوبن المجلدات والملفات على الشكل التالي
```
drf_course\  <--This is the root directory
    backend\
        docker\
            ...
        drf_course\
            >__init__.py
            >asgi.py
            >settings.py
            >urls.py
            >wsgi.py
        >manage.py
        >requirements.txt
    steps\
        ...
    venv\ <--New directory
        include\
        Lib\
        Scripts\
    >.env <--New file
    >.gitignore
    >docker-compose.yml
    >env.template
    >README.md
    >server.py
```

***
***
```
3) After Download Proceed with installation      MYSQLworkbench  حمل بعد الإنزال

4) Start A Database Connection     إبدأ الإتصال بعد الإنزال
![Alt text](https://github.com/basharourabi/django_course/blob/main/static_files/MySQLWorkbench_zqUHOFlbG8.png)


5) Enter Database Credentials & Settings for Database Connection       أدخل إعدادات الإتصال ونعريف المستخدم 
   ![Alt text](https://github.com/basharourabi/django_course/blob/main/static_files/ShareX_0CJwYMSi4V.png)



## Steps/Commands
You should now have a directory called 'drf_course' in your development directory. This will be known as your 'root directory'.

In this module, we will be start our project. To do this we will need to create a virtual environment.
>Note: Python virtual env docs can be found [here](https://docs.python.org/3/tutorial/venv.html).

1) Virtual Environment      ألبيئة الإفتراضية
- Open a terminal and use the following command to create a virtual environment. 
```
python -m venv venv
```
Now activate the virtual environment with the following command. تفعيل البيئة الإفتراضية
```
# windows machine
venv\Scripts\activate.bat

#mac/linux
source venv/bin/activate
```
You will know your virtual environment is active when your terminal displays the following:
سوف تعلم أن تفعيل البيئة الإفتراضية مفعلة لأن إسم البيئة بين قوسين على بداية سطر الأمر
```
(venv) path\to\project\drf_course>
```

2) Packages and requirements - Our project will rely on a whole bunch of 3rd party packages (requirements) to function. We will be using a Python package manager to install packages throughout this course. 
I have already created a requirements.txt file. Check out /backend/requirements.txt

 
 backend ووضعه بمجلد   (requirements.txt) لبرمجة البيئة الإفتراضية عليك إنشاء ملف يإسم
يجب الإلتزام برقم الإصدارات حيث تغيير إرتباط الإصدارات قد ىؤدي الى مشاكل  
```
asgiref==3.5.2
Django==4.1.3
django-extensions==3.2.1
django-filter==22.1
djangorestframework==3.14.0
djangorestframework-jsonapi==6.0.0
inflection==0.5.1
python-dotenv==0.21.0
pytz==2022.6
sqlparse==0.4.3
tzdata==2022.6
```
Let's go ahead and install our project requirements. Add the following code to you terminal.
لتفعيل البيئة الإفتراضية عليك  تثبيت ملف يإسم (requirements.txt) وتحديد موقعه من خلال تحديد اسم المجلد اللذي يحتويه


```
pip install -r backend/requirements.txt
```

3) Django - You can now go ahead and start a new Django project. Installing Django has given you access to a handy 'startproject' command. Use the following command to start our new project.
لتفعيل وتثلبيت مشروع منصة django عليك التثبيت من خلال الأوامر التالية 
```
django-admin startproject drf_course backend
```

4) Secrets and Environment Variables - It is good practice to separate sensitive information from your project. We have installed a package called 'python-dotenv' that helps us manage secrets easily. Lets go ahead and create a env file to store information that is specific to our working environment. Use the following command in your terminal.

المصطلحات والكلمات السرية المستخدمة يجب أن تفصل عن باقي ملفات المشروع، وعليه سوف ننشئ بيئة  إفتراضية  جديدة من الممكن فصلها لاحقا وتسمية هذه البيئة env. 

```
# windows machine
copy env.template .env

#mac/linux
cp env.template .env
```

You can use your new .env file to store API keys, secret_keys, app_passwords and you will gain access to these in the Django app.
***
***

## New Root directory
>Note: If all went well, your root directory should now look like this
إذا مشي كل شيئ علا ما يرام سوف يكون شكل تكوبن المجلدات والملفات على الشكل التالي
```
drf_course\  <--This is the root directory
    backend\
        docker\
            ...
        drf_course\
            >__init__.py
            >asgi.py
            >settings.py
            >urls.py
            >wsgi.py
        >manage.py
        >requirements.txt
    steps\
        ...
    venv\ <--New directory
        include\
        Lib\
        Scripts\
    >.env <--New file
    >.gitignore
    >docker-compose.yml
    >env.template
    >README.md
    >server.py
```

***
***
```
3) After Download Proceed with installation      MYSQLworkbench  حمل بعد الإنزال

4) Start A Database Connection     إبدأ الإتصال بعد الإنزال
![Alt text](https://github.com/basharourabi/django_course/blob/main/static_files/MySQLWorkbench_zqUHOFlbG8.png)


5) Enter Database Credentials & Settings for Database Connection       أدخل إعدادات الإتصال ونعريف المستخدم 
   ![Alt text](https://github.com/basharourabi/django_course/blob/main/static_files/ShareX_0CJwYMSi4V.png)



## Steps/Commands
You should now have a directory called 'drf_course' in your development directory. This will be known as your 'root directory'.

In this module, we will be start our project. To do this we will need to create a virtual environment.
>Note: Python virtual env docs can be found [here](https://docs.python.org/3/tutorial/venv.html).

1) Virtual Environment      ألبيئة الإفتراضية
- Open a terminal and use the following command to create a virtual environment. 
```
python -m venv venv
```
Now activate the virtual environment with the following command. تفعيل البيئة الإفتراضية
```
# windows machine
venv\Scripts\activate.bat

#mac/linux
source venv/bin/activate
```
You will know your virtual environment is active when your terminal displays the following:
سوف تعلم أن تفعيل البيئة الإفتراضية مفعلة لأن إسم البيئة بين قوسين على بداية سطر الأمر
```
(venv) path\to\project\drf_course>
```

2) Packages and requirements - Our project will rely on a whole bunch of 3rd party packages (requirements) to function. We will be using a Python package manager to install packages throughout this course. 
I have already created a requirements.txt file. Check out /backend/requirements.txt

 
 backend ووضعه بمجلد   (requirements.txt) لبرمجة البيئة الإفتراضية عليك إنشاء ملف يإسم
يجب الإلتزام برقم الإصدارات حيث تغيير إرتباط الإصدارات قد ىؤدي الى مشاكل  
```
asgiref==3.5.2
Django==4.1.3
django-extensions==3.2.1
django-filter==22.1
djangorestframework==3.14.0
djangorestframework-jsonapi==6.0.0
inflection==0.5.1
python-dotenv==0.21.0
pytz==2022.6
sqlparse==0.4.3
tzdata==2022.6
```
Let's go ahead and install our project requirements. Add the following code to you terminal.
لتفعيل البيئة الإفتراضية عليك  تثبيت ملف يإسم (requirements.txt) وتحديد موقعه من خلال تحديد اسم المجلد اللذي يحتويه


```
pip install -r backend/requirements.txt
```

3) Django - You can now go ahead and start a new Django project. Installing Django has given you access to a handy 'startproject' command. Use the following command to start our new project.
لتفعيل وتثلبيت مشروع منصة django عليك التثبيت من خلال الأوامر التالية 
```
django-admin startproject drf_course backend
```

4) Secrets and Environment Variables - It is good practice to separate sensitive information from your project. We have installed a package called 'python-dotenv' that helps us manage secrets easily. Lets go ahead and create a env file to store information that is specific to our working environment. Use the following command in your terminal.

المصطلحات والكلمات السرية المستخدمة يجب أن تفصل عن باقي ملفات المشروع، وعليه سوف ننشئ بيئة  إفتراضية  جديدة من الممكن فصلها لاحقا وتسمية هذه البيئة env. 

```
# windows machine
copy env.template .env

#mac/linux
cp env.template .env
```

You can use your new .env file to store API keys, secret_keys, app_passwords and you will gain access to these in the Django app.
***
***

## New Root directory
>Note: If all went well, your root directory should now look like this
إذا مشي كل شيئ علا ما يرام سوف يكون شكل تكوبن المجلدات والملفات على الشكل التالي
```
drf_course\  <--This is the root directory
    backend\
        docker\
            ...
        drf_course\
            >__init__.py
            >asgi.py
            >settings.py
            >urls.py
            >wsgi.py
        >manage.py
        >requirements.txt
    steps\
        ...
    venv\ <--New directory
        include\
        Lib\
        Scripts\
    >.env <--New file
    >.gitignore
    >docker-compose.yml
    >env.template
    >README.md
    >server.py
```

***
***
