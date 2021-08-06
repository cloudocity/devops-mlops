FROM continuumio/miniconda3:latest
WORKDIR /app
COPY 1.sh usr/src/app/
RUN pip install mlflow boto3 pymysql
CMD usr/src/app/1.sh