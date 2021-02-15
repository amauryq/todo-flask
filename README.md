# TODO App

## Installing Tool

$ cd todo-api
$ virtualenv flask
New python executable in flask/bin/python
Installing setuptools............................done.
Installing pip...................done.
$ flask/bin/pip install flask flask-httpauth

## Get All Tasks

### Insecure

curl -i http://localhost:5000/todo/api/v1.0/tasks

### Secure 

curl -u amauryq:password -i http://localhost:5000/todo/api/v1.0/tasks

## Get Specific Task

curl -i http://localhost:5000/todo/api/v1.0/tasks/2

## Create Task

curl -i -H "Content-Type: application/json" -X POST -d '{"title":"Read a book"}' http://localhost:5000/todo/api/v1.0/tasks

Windows
curl -i -H "Content-Type: application/json" -X POST -d "{"""title""":"""Read a book"""}" http://localhost:5000/todo/api/v1.0/tasks

## Update Task

curl -i -H "Content-Type: application/json" -X PUT -d '{"done":true}' http://localhost:5000/todo/api/v1.0/tasks/2