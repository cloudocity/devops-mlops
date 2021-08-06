## Домашняя работа к занятию “Docker и микросервисная архитектура”

## **Что сделанно**:
1.	За основу взят образ continuumio/miniconda3:latest
<br> ```FROM continuumio/miniconda3:latest```

2.	Рабочей папкой назначена /app 
      <br> ```WORKDIR usr/src/app/```
3.	Создан файл 1.sh, который выдавает надпись “Hello Netology”.
      <br> ```#!/bin/bash```
      <br> ```echo Hello Netology!```
4.	Копирование скрипта в контейнер
       <br> ```COPY 1.sh .```
5.	Установка дополнительных компонентов для python: mlflow boto3 pymysql.
      <br> ```RUN pip install mlflow boto3 pymysql```
6.	Запуск скрипта при запуске контейнера
      <br> ```CMD ./1.sh```


## **Лог выполнения сборки**: 
```(base) C:\PythonProjects\devops-mlops\Docker>docker build . -t netology-ml:netology-ml
(base) C:\PythonProjects\devops-mlops\Docker>docker build . -t netology-ml:netology-ml
[+] Building 32.1s (9/9) FINISHED
 => [internal] load build definition from Dockerfile                                                                                                                                                                                  0.0s
 => => transferring dockerfile: 156B                                                                                                                                                                                                  0.0s
 => [internal] load .dockerignore                                                                                                                                                                                                     0.0s
 => => transferring context: 2B                                                                                                                                                                                                       0.0s
 => [internal] load metadata for docker.io/continuumio/miniconda3:latest                                                                                                                                                              0.8s
 => [1/4] FROM docker.io/continuumio/miniconda3:latest@sha256:592a60b95b547f31c11dc6593832e962952e3178f1fa11db37f43a2afe8df8d7                                                                                                        0.0s
 => [internal] load build context                                                                                                                                                                                                     0.0s
 => => transferring context: 25B                                                                                                                                                                                                      0.0s
 => CACHED [2/4] WORKDIR usr/src/app/                                                                                                                                                                                                 0.0s
 => [3/4] COPY 1.sh .                                                                                                                                                                                                                 0.0s
 => [4/4] RUN pip install mlflow boto3 pymysql                                                                                                                                                                                       28.9s
 => exporting to image                                                                                                                                                                                                                2.3s
 => => exporting layers                                                                                                                                                                                                               2.2s
 => => writing image sha256:4baf27727e07aed9f1408ed3d45250baecac66d7c6626424018a1f0dd569c43a                                                                                                                                          0.0s
 => => naming to docker.io/library/netology-ml:netology-ml```  
