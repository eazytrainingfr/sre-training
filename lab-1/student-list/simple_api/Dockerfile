ARG VERSION="3.8-buster"
FROM python:$VERSION
#Maintainer of image
LABEL maintainer="EAZYTraining" email="eazytrainingfr@gmail.com"
#Install of dependencies
RUN apt update -y && apt install python3-dev libsasl2-dev libldap2-dev libssl-dev -y 
COPY requirements.txt student_age.py /
RUN pip3 install -r /requirements.txt
#CREATE DATA FOLDER
VOLUME /data
#EXPOSE PORT
EXPOSE 5000
#RUN CODE
CMD [ "python", "./student_age.py" ]
