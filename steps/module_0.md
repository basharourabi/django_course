Microservices Course - Module 0
I hope you like it.

> These notes follow on from the README.md getting started instructions.
***
Microservices Architecture                                  الهيكل البنيوي للخدمات السحابية المصغرة 

##-Definition                          Module 0 التعريف-

Unlike One Big Program (Monolithic) Microservice or the service is a related entity interms of functionality Such as order management, customer management; each microservice is a complete program (process) enclosed that requires an input or set of inputs and can deliver an output. A microservice is a complete program that is exposed or communicates to other microservices or external entities through an api request. 

الخدمة Service هي مجموعة من الخصائص المهام المتعلقة ببعضها في البرامج، مثلاً إدارة الطلبات Order Management، إدارة العملاء Customer Management، وهكذا. وكل خدمة مصغرة Microservices هي تعتبر مشروع كامل صغير ولديها داخلياً معمارية لها. بعض من هذه الخدمات المصغرة Microservices يمكن أن تقدم Expose API سوءاً للتطبيقات أو لخدمات مصغرة أخرى. وبعض هذه ال Microservices قد تكون هي Web UI. وفي وقت التشغيل كل من هذه الخدمات سوف تكون على VM لوحدها او Docker Container. الصورة التالية تبين شكل المشروع بعد تبني هذه الطريقة في العمل:



Environments                                                                البيئة الإفتراضية 


## Components                                    الاجزاء - Module 0
---
1- Computing Logic / Process     Python                 منطق المعالجة | العملية 
---
    1.1 Python Interpretor                               بايثون معالج 
    1.2 Python Libraries                                مكتبات بايثون
    1.3 Version Settings                                تحديد الإصدار 
---
2- Python Framework              Django           الية تشغيل بايثون للموق
---
    2.1 Page Templates                                  قوالب للصفحات 
    2.2 URL Routings                               توجيه عناوين الصفحات 
    2.3 APP Logic                                        منطق التطبيق
    2.4 Models                                           تحديد النماذج  
    2.5 Views                                            تحديد المشاهد  
---
3- Web Server                    NGINX                    خادم مواقع 
---

    3.1 Page Templates                                  قوالب للصفحات 
    3.2 URL Routings                               توجيه عناوين الصفحات 
    3.3 APP Logic                                        منطق التطبيق
    3.4 Models                                           تحديد النماذج  
    3.5 Views                                            تحديد المشاهد  
---
***

## Environments                                                  البيئة الإفتراضية ##
---
![Architecture Block](https://github.com/basharourabi/django_course/blob/main/static_files/AppParadigm.jpg)
---

***
Challenges for new Coders                                  المعضلات و التحديات للمبرمجين الحديثين والجدد
Environments                                                                    البيئة الإفتراضية
# Environments                                        البيئة الإفتراضية - Module 0

***
## You may have tons of questions on this subject matter, but essentialy the process of setting the environment is construed of three steps.
### 1-Include a requirements.txt file in the filing structure


### ارفاق ملف تكست ينص أسماء التطبيقات وتحديد إصدارها ( تحديد الإصدارات مصدر معظم المشكلات - قد لا تتماشا بعض الإصدارات مع أخرى أو قد تتطلب طريقة اخرى في البرمجة)   
# 2-Inducing (adding) an environment file (setting up an env file)

3-Activating the environment file

```
drf_course\  <--This is the root directory <--المجلد الجذري
    backend\
        docker\
            ...
        >requirements.txt   <--This is the requirements file that is activated in the new virtual environment  <--الملف متطلبات الثطبيتات و البرامج التي تخضع لها البيئة 
    steps\
        ...
    >.gitignore
    >docker-compose.yml
    >env.template
    >README.md
    >server.py
```

If in doubt, run the following git commands:
```
git checkout module_1
git pull origin module_1
```

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
