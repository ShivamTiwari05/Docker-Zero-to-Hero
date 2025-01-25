FROM ubuntu

WORKDIR /app

COPY requirements.txt /app

COPY devops /app

RUN apt-get update && \
    apt-get install -y python3 python3-pip && \
    apt-get install -y pipx && \
    pip install --no-cache-dir -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3"]

CMD ["manage.py", "runserver", "0.0.0.0:8000"]