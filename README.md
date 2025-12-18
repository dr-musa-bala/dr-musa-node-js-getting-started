# nodejs-getting-started

A barebones Node.js app using [Express](https://expressjs.com/).

This application supports the tutorials for both the [Cedar and Fir generations](https://devcenter.heroku.com/articles/generations) of the Heroku platform. You can check them out here:

* [Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs)
* [Getting Started on Heroku Fir with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs-fir)

## Running Locally

Make sure you have [Node.js](http://nodejs.org/) and the [Heroku CLI](https://cli.heroku.com/) installed.

```sh
$ git clone https://github.com/heroku/nodejs-getting-started.git # or clone your own fork
$ cd nodejs-getting-started
$ npm install
$ npm start
```

Your app should now be running on [localhost:5006](http://localhost:5006/).

## Deploying to Heroku

Using resources for this example app counts towards your usage. [Delete your app](https://devcenter.heroku.com/articles/heroku-cli-commands#heroku-apps-destroy) and [database](https://devcenter.heroku.com/articles/heroku-postgresql#removing-the-add-on) as soon as you are done experimenting to control costs.

### Deploy on [Cedar][cedar]

By default, apps use Eco dynos on [Cedar][cedar] if you are subscribed to Eco. Otherwise, it defaults to Basic dynos. The 
Eco dynos plan is shared across all Eco dynos in your account and is recommended if you plan on deploying many small apps 
to Heroku. Learn more about our low-cost plans [here](https://blog.heroku.com/new-low-cost-plans).

Eligible students can apply for platform credits through our new [Heroku for GitHub Students program](https://blog.heroku.com/github-student-developer-program).

```
$ heroku create
$ git push heroku main
$ heroku open
```

### Deploy on [Fir][fir]

By default, apps on [Fir][fir] use 1X-Classic dynos. To create an app on [Fir][fir] you'll need to 
[create a private space](https://devcenter.heroku.com/articles/working-with-private-spaces#create-a-private-space)
first.

```
$ heroku spaces:create <space-name> --team <team-name> --generation fir
$ heroku create --space <space-name>
$ git push heroku main
$ heroku open
```

## Documentation

For more information about using Node.js on Heroku, see these Dev Center articles:

- [Getting Started on Heroku with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs)
- [Getting Started on Heroku Fir with Node.js](https://devcenter.heroku.com/articles/getting-started-with-nodejs-fir)
- [Heroku Node.js Support](https://devcenter.heroku.com/articles/nodejs-support)
- [Node.js on Heroku](https://devcenter.heroku.com/categories/nodejs)
- [Best Practices for Node.js Development](https://devcenter.heroku.com/articles/node-best-practices)
- [Using WebSockets on Heroku with Node.js](https://devcenter.heroku.com/articles/node-websockets)

[cedar]: https://devcenter.heroku.com/articles/generations#cedar
[fir]: https://devcenter.heroku.com/articles/generations#fir

## CI/CD Pipeline

This project uses GitHub Actions to implement a full CI/CD pipeline:
- Installs dependencies
- Runs automated tests
- Builds a Docker image
- Pushes the image to Docker Hub securely using GitHub Secrets

# Node.js CI/CD Pipeline with Docker & AWS EC2

## 📌 Overview
This project demonstrates a complete CI/CD pipeline using GitHub Actions.

Every push to the `main` branch automatically:
- Runs tests
- Builds a Docker image
- Pushes the image to Docker Hub
- Deploys the application to an AWS EC2 instance

## 🛠 Tech Stack
- Node.js (Express)
- Docker
- GitHub Actions
- Docker Hub
- AWS EC2 (Ubuntu)

## 🚀 Deployment Flow
1. Code pushed to GitHub
2. GitHub Actions runs CI/CD pipeline
3. Docker image is built and pushed to Docker Hub
4. EC2 pulls the latest image
5. Container is restarted automatically

## 🌍 Live Application
http://http://184.73.71.90/

## 👨‍💻 Author
**Dr. Musa Bala**
## ✅ Status
✔ CI/CD pipeline implemented  
✔ Docker image versioned (v1.0.0)  
✔ Automatically deployed to AWS EC2  
✔ Live production container running  

Latest stable version: **v1.0.0**
