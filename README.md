# sd-finalproject3
Enjoy !

## Prerequisites
+ Docker
+ Kubernetes
+ Minikube as a local environment


First Dockerized both frontend and backend with an node:alpine image as base an then installing dependencies and running it. Then i pushed them to docker hub to use them with kubernetes

Then for the CouchDB image, struggled with its init configuration since it doesn't run out of the box, for that it was necessary to add env vars with user credentials when running the database image 

Then wrote deployments and services in kubernetes having a load balancer on the front-end deployment to have an external ip where to access it and the rest. Reading couchDB documentation opted for setting user and passwords as env variables in yml file

Last for the backend deployment which is dependant of the database to work, it was necessary to add an env variable to connect with database


Then proceeded to apply all resources and used minikube to know the frontend url

