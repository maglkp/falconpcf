# falconpcf
Simple backend app template for PCF using Falcon framework for python

## Launching the app locally (example commands for Ubuntu/Debian)
* install git, python and virtualenv `sudo apt-get install virtualenv`
* create a python 3 virtual env `virtualenv venv -p /usr/bin/python3` (not strictly needed but gives better confidence that app would work in the cloud)
* activate the environment `source venv/bin/activate` (`venv\Scripts\activate.bat` on windows)
* install the requirements `pip install -r requirements.txt`
* run `gunicorn main:app`

## Running in Pivotal Cloud Foundry
* install cf cli (command line utils to interact with PCF) https://github.com/cloudfoundry/cli#downloads or https://docs.cloudfoundry.org/cf-cli/install-go-cli.html
* create an account in Pivotal https://run.pivotal.io/

## Instructions
* Clone this repo: 
* Open a shell and change into the `cf-HelloWorld` folder
* Login to Cloud Foundry: `cf login`
  * if using Pivotal Web Services use `api.run.pivotal.io` as the target
* Modify the application name in `manifest.yml` to be unique
* push the application to Cloud Foundry with: `cf push`

### Similar examples
* https://github.com/vchrisb/cf-HelloWorld
* https://github.com/swisscom/cf-sample-app-python
* https://www.digitalocean.com/community/tutorials/how-to-deploy-falcon-web-applications-with-gunicorn-and-nginx-on-ubuntu-16-04
