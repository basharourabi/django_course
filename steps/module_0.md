### Microservices Course - Module 0
I hope you like it.

> These notes follow on from the README.md getting started instructions.
***
Microservices Architecture                                  الهيكل البنيوي للخدمات السحابية المصغرة 

## Definition                          Module 0 التعريف-

Unlike One Big Program (Monolithic) Microservice or the service is a related entity interms of functionality Such as order management, customer management; each microservice is a complete program (process) enclosed that requires an input or set of inputs and can deliver an output. A microservice is a complete program that is exposed or communicates to other microservices or external entities through an api request. 

الخدمة Service هي مجموعة من الخصائص المهام المتعلقة ببعضها في البرامج، مثلاً إدارة الطلبات Order Management، إدارة العملاء Customer Management، وهكذا. وكل خدمة مصغرة Microservices هي تعتبر مشروع كامل صغير ولديها داخلياً معمارية لها. بعض من هذه الخدمات المصغرة Microservices يمكن أن تقدم Expose API سوءاً للتطبيقات أو لخدمات مصغرة أخرى. وبعض هذه ال Microservices قد تكون هي Web UI. وفي وقت التشغيل كل من هذه الخدمات سوف تكون على VM لوحدها او Docker Container. الصورة التالية تبين شكل المشروع بعد تبني هذه الطريقة في العمل:
## Subparts                                  الاجزاء لثانوية  - Module 0
---
1- Computing Logic / Process     Python                 منطق المعالجة | العملية 
---
    1.1 Python Interpretor                               بايثون معالج 
    1.2 Python Libraries                                مكتبات بايثون
    1.3 Version Settings                                تحديد الإصدار 
---


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
    2.6 User Management                                إدارة المستخدمين
---
3- Web Server                    NGINX                    خادم مواقع 
---

    3.1 Cashing                                         الذاكرة التصفحية  
    3.2 Load Balancing                                    موازنة الأداء    
    3.3 SSL Terminate                                    شهادات الأمنية 
    3.4 Static File Delivery                          تفديم الملفات الثابتة    
    3.5 Pages View Delivery                          الصفحات تفديم مشاهد  
---
***

## Environments                                                  البيئة الإفتراضية ##
---
![Architecture Block](https://github.com/basharourabi/django_course/blob/main/static_files/AppParadigm.jpg)
---

***

