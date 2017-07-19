# basic-flask-restful
Simple example app for how to deploy a web app using Python 3 and Flask-RESTful

## About
I find myself frequently spinning up microservices for work, IoT projects, etc. and have come to
really like working with Python 3.x and a library called [Flask-RESTful](http://flask-restful.readthedocs.io/en/0.3.5/).
Since I couldn't find basic starter code, I thought I would publish this to avoid always having
to rebuild from scratch all of the files necessary to deploy successfully to Bluemix.

## Deploy
### How to deploy, the tl;dr version
1. Log into Bluemix using the Cloud Foundry CLI
2. Change the name of the app in the manifest
3. Push using the the CLI

### How to deploy, the long version
1. Download and install the Cloud Foundry Command-Line Interface (https://docs.cloudfoundry.org/cf-cli/install-go-cli.html)
2. Set the CF CLI to point to Bluemix using this command: `cf api https://api.ng.bluemix.net`
3. Log into your Bluemix account using this command: `cf login` (You may need to specify some options)
4. Change line 3 of the `manifest.yml` file, replacing `basic-flask-restful` with your desired subdomain for Bluemix
5. Push to Bluemix using the CF CLI by using this command: `cf push`