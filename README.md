# docker-react

A React frontend application deployed using Docker and AWS Elastic Beanstalk.

## Table of Contents

* Project Overview
* Features
* Getting Started
* Docker Usage
* Deployment
* Environment Variables
* Testing
* License

## Project Overview

This project is a React frontend app, containerized with Docker and deployed to AWS Elastic Beanstalk. It demonstrates:

* Building a React app with Docker
* Running the app locally and in production environments
* CI/CD deployment using GitHub Actions
* Using AWS Elastic Beanstalk for cloud hosting

## Features

* React frontend
* Dockerized for consistent deployment
* CI/CD ready via GitHub Actions
* Cloud deployment with AWS Elastic Beanstalk

## Getting Started

Clone the repository:

```
git clone https://github.com/jaredto/docker-react.git
cd docker-react
```

Install dependencies:

```
npm install
```

Start the development server:

```
npm start
```

Your app should be running locally at `http://localhost:3000`.

## Docker Usage

### Build the Docker image

```
docker build -t docker-react-app .
```

### Run the container locally

```
docker run -p 8080:80 docker-react-app
```

### Docker Compose (Development)

```
docker-compose -f docker-compose-dev.yml up
```

Note: This runs the dev web server and tests

Stop containers:

```
docker-compose -f docker-compose-dev.yml down
```

## Deployment

This app is deployed to AWS Elastic Beanstalk using GitHub Actions.

* Each push to the `master` branch triggers a deployment workflow
* The workflow builds the Docker image, creates a ZIP package, and deploys it to EB
           |

## Testing

Run React tests:

```
npm test -- --coverage
```

## License

[MIT License](LICENSE)
