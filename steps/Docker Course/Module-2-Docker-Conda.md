<div style="display: flex; justify-content: space-between;">

<div style="width: 45%;">

# Docker Anaconda (Docker) Course - Module 2

This is my Docker course. I hope you like it.

> These notes follow on from the README.md getting started instructions.
***
***

## Docker Conda
To download Docker with anaconda image

>Steps/Commands
You should now have a directory called 'drf_course' in your development directory. This will be known as your 'root directory'.

Docker is an open platform for developers and system administrators to build, ship, and run distributed applications, whether on laptops, data center virtual machines, or the cloud. Anaconda, Inc. provides Anaconda and Miniconda Docker images.

>Read the official Docker documentation and specifically the information related to Docker Conda image and installation.

\```
https://docs.anaconda.com/free/anaconda/applications/docker/
\```
Begin by browsing the available Anaconda images on our Docker profile.

To obtain a fully working Anaconda image:

In a terminal window, run this command to display a list of available images:

\```
docker search continuumio
\```
Pull the desired image:
\```
docker pull continuumio/miniconda3
\```
Create a container using the image:
\```
docker run -t -i continuumio/miniconda3 /bin/bash
\```
This gives you direct access to the container where the conda tool is already available.

Test the container:

\```
conda info
\```
You now have a fully working Anaconda image.

</div>

<div style="width: 45%; text-align: right; direction: rtl;">

# دورة دوكر أناكوندا (دوكر) - الوحدة الثانية

هذه هي دورتي في دوكر. أتمنى أن تعجبك.

> تتبع هذه الملاحظات التعليمات الأولية في ملف README.md.
***
***

## تشغيل أناكوندا بداخل Docker
حمل صورة لنظام دوكر يشمل أناكوندا 

> الخطوات/الأوامر
يجب أن يكون لديك الآن دليل باسم 'drf_course' في دليل التطوير الخاص بك. سيعرف هذا كدليلك الجذري.

دوكر هو منصة مفتوحة للمطورين ومسؤولي النظام لبناء وشحن وتشغيل التطبيقات الموزعة، سواء على الحواسيب المحمولة أو الأجهزة الظاهرية في مراكز البيانات أو السحابة. توفر Anaconda, Inc. صور دوكر لأناكوندا ومينيكوندا.

> اقرأ الوثائق الرسمية لدوكر وبالتحديد المعلومات المتعلقة بصورة دوكر أناكوندا والتثبيت.

\```
https://docs.anaconda.com/free/anaconda/applications/docker/
\```
ابدأ بتصفح الصور المتاحة لأناكوندا على ملفنا الشخصي في دوكر.

للحصول على صورة أناكوندا تعمل بشكل كامل:

في نافذة الطرفية، قم بتشغيل هذا الأمر لعرض قائمة بالصور المتاحة:

\```
docker search continuumio
\```
اسحب الصورة المطلوبة:
\```
docker pull continuumio/miniconda3
\```
أنشئ حاوية باستخدام الصورة:
\```
docker run -t -i continuumio/miniconda3 /bin/bash
\```
هذا يعطيك إمكانية الوصول المباشر إلى الحاوية حيث أداة كوندا متاحة بالفعل.

اختبر الحاوية:

\```
conda info
\```
لديك الآن صورة أناكوندا تعمل بشكل كامل.

</div>

</div>
