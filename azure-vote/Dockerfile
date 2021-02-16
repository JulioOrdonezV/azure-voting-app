FROM    tiangolo/uwsgi-nginx-flask:python3.8

RUN     apt-get update && \
        apt-get install default-libmysqlclient-dev -y && \
        pip install --upgrade pip && \
        pip install flask-mysql
 
ADD     /azure-vote /app
