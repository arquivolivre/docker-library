FROM python:2.7

RUN pip install -U ara pymysql

CMD ["ara-manage", "runserver", "-h", "0.0.0.0", "-p", "8080"]

EXPOSE 8080
