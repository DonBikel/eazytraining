ARG VERSION="3.13.0-bullseye"
FROM python:$VERSION
LABEL maintainer="Bikel" email="keumekabik@gmail.com"
RUN apt update -y && apt install python3-dev libsasl2-dev libldap2-dev libssl-dev -y 
COPY requirements.txt student_age.py /
COPY student_age.json /data/
RUN pip3 install -r /requirements.txt
VOLUME /data
EXPOSE 5000
CMD [ "python3", "./student_age.py" ]
