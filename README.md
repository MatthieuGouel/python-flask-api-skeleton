# Python3 Flask Rest API skeleton

[![Build Status](https://travis-ci.org/matthieugouel/python-flask-api-skeleton.svg?branch=master)](https://travis-ci.org/matthieugouel/python-flask-api-skeleton)
[![Coverage Status](https://img.shields.io/coveralls/github/matthieugouel/python-flask-api-skeleton.svg)](https://coveralls.io/github/matthieugouel/python-flask-api-skeleton)
[![license](https://img.shields.io/github/license/matthieugouel/python-flask-api-skeleton.svg)](https://github.com/matthieugouel/python-flask-api-skeleton/blob/master/LICENSE)

This project is a skeleton of a Flask-restplus API. It tends to be modular in order to add *plugins* for larger projects (databases, sessions, async requests...)

## Installation

Note : The installation into a virtualenv is heavily recommended.

If you want to install the package :

```
pip install .
```

For development purposes, you can install the package in editable mode with the dev requirements.

```
pip install -e . -r requirements-dev.txt
```

## Usage

To start the application, you can use the file run.py :

```
python run.py
```

Then, you can access to the api in localhost :

```
curl -X GET -H "Content-Type: application/json" localhost:5000/api/hello/test
```

## Usage with Docker

To use it in a Docker container, just build it :

```
docker build -t skeleton_api .
```

Then run it :

```
docker run -p 127.0.0.1:5000:80 skeleton_api
```

## Syntax

You can check the syntax using flake8 (you must have flake8 package installed first) :

```
flake8 api
```

You can also use tox (you must have tox package installed first) :

```
tox -e lint
```

## Test coverage

To execute the test coverage, you must install the package with the dev requirements (see installation section).

Then, you can run the coverage with the following command :

```
coverage run --source api -m py.test
```

You can also use tox (you must have tox package installed first) :

```
tox -e test
```
