# Solving Insight DevOps Engineering Systems Puzzle

## Table of Contents
1. [My Strategy for Solving the Puzzle](README.md#my-strategy-for-solving-the-puzzle)
2. [Develop Architecture without Docker](README.md#develop-architecture-without-docker)
3. [Learn how Docker Compose fit in](README.md#learn-how-docker-compose-fit-in)
4. [Challenges](README.md#challenges)

# My Strategy for Solving the Puzzle

1) Learn the Basics
2) Develop Architecture without Docker - Python -> Flask/NginX -> PostgreSQL
3) Learn how Docker Compose fit into this archtitecture

# Learn the Basics

1) Existing Knowledge
    * multi-tier architecture
    * other computer languages like Java & Javascript
    * other web servers like Tomcat Apache
    * SQL database like MySQL & ORM tools
2) Missing Knowledge
    * Need to learn python, flask, nginx, docker, docker-compose

3) git clone system puzzle repo & see the Errors after running docker commands as instructed.
4) Install Docker on my MacOS.
5) Watch a couple short YouTube videos about Docker & Docker Compose
    * learn about Docker Hub
    * learn about Dockerfile, Requirements.txt, docker-compose.yml, etc.
6) Hack around the files with PORT numbers a bit with no success.

# Develop Architecture without Docker

1) Creating a Simple Flask Web Application
    * install python3
    * install Flask
    * create a simple hello.py
    * see result web page on 0.0.0.0:5000

2) Create a Simple Python/Flask (with Flask WTForms) and PostGreSQL Web Application
    * install PostgreSQL 10
    * pip3 install psycopg2 (database driver)
    * pip install sqlalchemy (ORM)
    * pip install flask-WTF

3) Configure NGINX for a Flask Web Application
    * brew install nginx
    * pip3 install gunicorn
    * gunicorn app:app -b localhost:8080

# Learn how Docker Compose fit in

1) Learn more about Docker terminology - Dockerfile, Image, Container, etc.
2) Learn about Docker Legacy Archtirecture (one Container (Dockerfile) for each Process)
3) Learn about Docker Compose as an Orchestration Tool
4) Learn about User-Defined Network (ie. Bridge Network)
5) Learn some Docker commands used for Debugging 
    * docker container ls
    * docker rm -f <container-name>
    * docker volume rm $(docker volume ls -q)

6) Refresh some Linux commands used for Debugging
    * netstat -abn | grep 8080"
    * sudo lsof -i:80
    * ps -ef | grep <PID>
    * kill -9 <PID>
    * ping localhost
    * sudo apachectl -k stop
    * sudo launchctl unload -w /System/Library/LaunchDaemons/org.apache.httpd.plist"

# Challenges
   * Online Docker/Docker Compose Documentation is somewhat confusing
    - Found various articles related to older version of Docker vs. Docker Compose & cause some confusion.
    
   * Port 8080 is occupied by Apache2 vHost & cause new PORT errors that were confusing with the original PORT errors.
