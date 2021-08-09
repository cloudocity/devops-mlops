## Домашняя работа к занятию “Docker и микросервисная архитектура”

## **Что сделанно**:
1.	За основу взят образ continuumio/miniconda3:latest
<br> ```FROM continuumio/miniconda3:latest```

2.	Рабочей папкой назначена /app 
      <br> ```WORKDIR app/```
3.	Создан файл 1.sh, который выдавает надпись “Chip & Dale”.
      <br> ```#!/bin/bash```
      <br> ```echo "Chip & Dale"```
      
4.	Установка дополнительных компонентов для python: mlflow boto3 pymysql.
      <br> ```RUN pip install mlflow boto3 pymysql```
5.	Копирование скрипта в контейнер
       <br> ```COPY 1.sh .```
6.	Назначение прав на скрипт
       <br> ```RUN chmod 777 ./1.sh```
7.	Запуск скрипта при запуске контейнера
      <br> ```CMD ./1.sh```


## **Лог выполнения сборки**: 
```
(base) C:\PythonProjects\devops-mlops\Docker>docker build . -t netology-ml:netology-ml
[+] Building 1.0s (9/9) FINISHED
 => [internal] load build definition from Dockerfile                                                                                                                                                                                  0.0s
 => => transferring dockerfile: 31B                                                                                                                                                                                                   0.0s
 => [internal] load .dockerignore                                                                                                                                                                                                     0.0s
 => => transferring context: 2B                                                                                                                                                                                                       0.0s
 => [internal] load metadata for docker.io/continuumio/miniconda3:latest                                                                                                                                                              0.7s
 => [1/4] FROM docker.io/continuumio/miniconda3:latest@sha256:592a60b95b547f31c11dc6593832e962952e3178f1fa11db37f43a2afe8df8d7                                                                                                        0.0s
 => [internal] load build context                                                                                                                                                                                                     0.1s
 => => transferring context: 61B                                                                                                                                                                                                      0.0s
 => CACHED [2/4] WORKDIR app/                                                                                                                                                                                                         0.0s
 => CACHED [3/4] RUN pip install mlflow boto3 pymysql                                                                                                                                                                                 0.0s
 => [4/4] COPY 1.sh .                                                                                                                                                                                                                 0.0s
 => exporting to image                                                                                                                                                                                                                0.0s
 => => exporting layers                                                                                                                                                                                                               0.0s
 => => writing image sha256:741127d3ddfe216a23b65d5ed4f4ab661773afe505b8ea76c74d6ce38337b628                                                                                                                                          0.0s
 => => naming to docker.io/library/netology-ml:netology-ml             ```  
