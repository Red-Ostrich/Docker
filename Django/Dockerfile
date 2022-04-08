FROM python:3
ENV PYTHONUNBUFFERED=1
RUN mkdir /app
WORKDIR /app
RUN apt-get clean && apt-get update && apt-get install -y locales
RUN locale-gen en_US.UTF-8
RUN export LC_ALL="en_US.UTF-8"
RUN export LC_CTYPE="en_US.UTF-8"
RUN dpkg-reconfigure locales --force
COPY requirements.txt /app/
RUN pip install -r requirements.txt
COPY . /app/
