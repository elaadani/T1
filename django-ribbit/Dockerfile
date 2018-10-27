FROM ubuntu:latest

workdir /ribbit

copy . /ribbit
run apt-get -y update
run apt-get -y install python
run apt-get -y install python-pip
run pip install virtualenv
run pip install -r requeriments.txt
run virtualenv --no-site-packages ribbit_env

run python manage.py syncdb --noinput
run python manage.py migrate ribbit_app

cmd python manage.py runserver 0:$PORT