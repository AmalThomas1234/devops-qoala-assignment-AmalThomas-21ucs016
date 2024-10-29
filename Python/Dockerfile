FROM python:3.9

WORKDIR /appp

COPY app.py /app

RUN pip install flask netifaces

EXPOSE "8000"

CMD ["python", "app.py"]
