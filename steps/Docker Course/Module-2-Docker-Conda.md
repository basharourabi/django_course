# Docker and Anaconda Guide

> دليل دوكر وأناكوندا

## Introduction

> مقدمة

Docker is an open platform for developers and system administrators to build, ship, and run distributed applications, whether on laptops, data center virtual machines, or the cloud. Anaconda, Inc. provides Anaconda and Miniconda Docker images.

> دوكر هو منصة مفتوحة للمطورين ومسؤولي النظام لبناء وشحن وتشغيل التطبيقات الموزعة، سواء على أجهزة الكمبيوتر المحمولة أو الأجهزة الظاهرية في مراكز البيانات أو السحابة. توفر شركة أناكوندا، المحدودة صور دوكر لأناكوندا ومينيكوندا.

Read the official Docker documentation and specifically the information related to Docker images.

> اقرأ الوثائق الرسمية لدوكر وبالتحديد المعلومات المتعلقة بصور دوكر.

Begin by browsing the available Anaconda images on our Docker profile.

> ابدأ بتصفح الصور المتاحة لأناكوندا على ملفنا الشخصي في دوكر.

## Steps to Obtain a Working Anaconda Image

> الخطوات للحصول على صورة أناكوندا تعمل

To obtain a fully working Anaconda image:

> للحصول على صورة أناكوندا تعمل بشكل كامل:

1) In a terminal window, run this command to display a list of available images:

> 1) في نافذة الطرفية، قم بتشغيل هذا الأمر لعرض قائمة بالصور المتاحة:

> لتفعيل خساب على دوكر
```
docker search continuumio
```

2) Download the desired Docker Anaconda Image     
Full Documentation on Docker Desktop & Download Link

>2) في نافذة الطرفية، قم بتشغيل هذا الأمر لنسخ الصور المطلوبة لأناكوندا :

-Goto
```
docker pull continuumio/miniconda3
```


> These notes follow on from the README.md getting started instructions.
***
***

