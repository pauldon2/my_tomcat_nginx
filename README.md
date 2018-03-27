## Bring up containers

From project root directory

`docker-compose build --no-cache`  
`docker-compose up -d`

## Bringing down containers

`docker-compose down`   

## Accessing tomcat 

In web browser go to http://localhost.  You can change port in the docker-compose.yml file.  Find this line:

`- "80:80"`

Change 80 to any unused port

## Accessing hello world war file

By default this container will have the sample.war (hello world). You should be able to go to the following url to access:

http://localhost/sample/

## Changing to deploy a different war file on startup

Put your actual war file into the tomcat/webapps directory and then edit the tomcat/Dockerfile, changing the sample.war file to your new war file:

`ADD sample.war /usr/local/tomcat/webapps/`

change to 

`ADD warfile.war /usr/local/tomcat/webapps/`

## Deploying a war file through the manager

Go to your manager app (username: admin, password: admin) and you'll see a section for uploading your war file.

In your browser, go to the server running docker,  http://localhost/manager/html

Manager app username and password can be found in the tomcat/context.xml directory if you want to change
