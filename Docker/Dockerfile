FROM continuumio/miniconda3:latest
WORKDIR usr/src/app/
COPY 1.sh .
RUN pip install mlflow boto3 pymysql
CMD ./1.sh