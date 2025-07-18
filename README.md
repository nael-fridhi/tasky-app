# Tasky App
Tasky application is a task management app developed using Golang and MongoDB as Database. It's used as a testing app for our Google Cloud services hands-on quickstart.

[![build](https://github.com/nael-fridhi/tasky-app/actions/workflows/tasky-cicd.yml/badge.svg)](https://github.com/nael-fridhi/tasky-app/actions/workflows/tasky-cicd.yml) ![codecov](https://codecov.io/gh/nael-fridhi/tasky-app/graph/badge.svg)
![](https://img.shields.io/badge/golang-v1.18-blue)
![](https://img.shields.io/badge/docs-in_progress-orange)
![linesofcode](https://aschey.tech/tokei/github/nael-fridhi/tasky-app)
![](https://img.shields.io/badge/license-MIT-violet)

---

## Docker
A Dockerfile has been provided to run this application.  The default port exposed is 8080. Also you can find K8s resources to deploy the application to Google Kubernetes Engine.

![](./k8s.svg)

## Environment Variables
The following environment variables are needed.
|Variable|Purpose|example|
|---|---|---|
|`MONGODB_URI`|Address to mongo server|`mongodb://servername:27017` or `mongodb://username:password@hostname:port` or `mongodb+srv://` schema|
|`SECRET_KEY`|Secret key for JWT tokens|`secret123`|

Alternatively, you can create a `.env` file and load it up with the environment variables.

## Running with Go

Clone the repository into a directory of your choice Run the command `go mod tidy` to download the necessary packages.

You'll need to add a .env file and add a MongoDB connection string with the name `MONGODB_URI` to access your collection for task and user storage.
You'll also need to add `SECRET_KEY` to the .env file for JWT Authentication.

Run the command `go run main.go` and the project should run on `locahost:8080`

## License

This project is licensed under the terms of the MIT license.

Original project: https://github.com/dogukanozdemir/golang-todo-mongodb