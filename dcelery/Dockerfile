FROM python:3.11.2-alpine 

WORKDIR /usr/src/app

#   prevent from writing .pyc files
ENV PYTHONWRITEBYTECODE 1

#   prevent from buffering stdout and stderr
ENV PYTHONUNBUFFERED 1

RUN pip install --upgrade pip
COPY ./requirements.txt /usr/src/app/requirements.txt
RUN pip install -r requirements.txt 

COPY ./entrypoint.sh /usr/src/app/entrypoint.sh

COPY . /usr/src/app/

ENTRYPOINT [ "/usr/src/app/entrypoint.sh" ]