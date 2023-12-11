## For running the application on localhost

In each service folder, Go to .env.dev (development environment) file :
1. Make sure to assign a MONGODB URI Link. You can generate your own cluster from [here](https://www.mongodb.com)
2. MSG_QUEUE_URL should be replaced with your Amazon MQ broker service endpoint
3. Feel free to use your custom port. Make sure to expose the same Port numbers in the Docker files also.

Download the node modules in each working directory using **npm install** 

**For running gateway-service** : node index.js
**For running customer-service** : npm run dev
**For running product-service** : npm run dev
**For running shopping-service** : npm run dev
**For running Frontend-service** : npm start (use **sudo** if required)

## For running the application on AWS

In gateway directory,

1. Run **docker build -t gateway-service .**
2. This creates a docker image and then push this docker image to AWS ECR service using **docker push**
3. For this, We have exposed PORT 8000

In product directory,

1. Run **docker build -t product-service .**
2. This creates a docker image and then push this docker image to AWS ECR service using **docker push**
3. For this, We have exposed PORT 8002

In customer directory,

1. Run **docker build -t customer-service .**
2. This creates a docker image and then push this docker image to AWS ECR service using **docker push**
3. For this, We have exposed PORT 8001

In shopping directory,

1. Run **docker build -t shopping-service .**
2. This creates a docker image and then push this docker image to AWS ECR service using **docker push**
3. For this, We have exposed PORT 8003
   
In microservice_frontend directory,

1. Run **docker build -t frontend-service .**
2. This creates a docker image and then push this docker image to AWS ECR service using **docker push**
3. For this, We have exposed PORT 80

Finally,
1. Create a cluster using AWS ECS service
2. Create task definitions for these.
3. Run new tasks in the cluster based on the newly created task definitions.
4. Make sure to use the PORT number you have exposed in the Docker files.
5. You can directly run the frond-end service task on PORT 80. No need to add any extra configurations.








