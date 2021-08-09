FROM continuumio/miniconda3:latest
WORKDIR app/
RUN pip install mlflow boto3 pymysql
COPY 1.sh .
RUN chmod 777 ./1.sh
CMD ./1.sh
