FROM scratch
ADD alpine-minirootfs-3.11.12-x86_64.tar.gz  /
RUN dir
EXPOSE 8000
RUN apk add --update python3 python3-dev py3-pip build-base
COPY . /backend
WORKDIR /backend 
COPY requirements.txt requirements.txt
RUN python3 -m pip install -r requirements.txt
COPY . .
ENTRYPOINT [ "python3","manage.py","runserver","0.0.0.0:8000"]