| English Content | Arabic Content |
|-----------------|----------------|
| # Docker Anaconda (Docker) Course - Module 2 <br> This is my Docker course. I hope you like it. <br> > These notes follow on from the README.md getting started instructions. | # دورة دوكر أناكوندا (دوكر) - الوحدة الثانية <br> هذه هي دورتي في دوكر. أتمنى أن تعجبك. <br> > تتبع هذه الملاحظات التعليمات الأولية في ملف README.md. |
| *** <br> *** | *** <br> *** |
| Docker is an open platform for developers and system administrators to build, ship, and run distributed applications, whether on laptops, data center virtual machines, or the cloud. Anaconda, Inc. provides Anaconda and Miniconda Docker images.

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

conda info
You now have a fully working Anaconda image.| ## تشغيل أناكوندا بداخل Docker <br> حمل صورة لنظام دوكر يشمل أناكوندا <br> >الخطوات/الأوامر <br> يجب أن يكون لديك الآن دليل باسم 'drf_course' في دليل التطوير الخاص بك. سيعرف هذا كدليلك الجذري. <br> دوكر هو منصة مفتوحة للمطورين ومسؤولي النظام لبناء وشحن وتشغيل التطبيقات الموزعة، سواء على الحواسيب المحمولة أو الأجهزة الظاهرية في مراكز البيانات أو السحابة. توفر Anaconda, Inc. صور دوكر لأناكوندا ومينيكوندا. <br> >اقرأ الوثائق الرسمية لدوكر وبالتحديد المعلومات المتعلقة بصورة دوكر أناكوندا والتثبيت. <br> `https://docs.anaconda.com/free/anaconda/applications/docker/` |
