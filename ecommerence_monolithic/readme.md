## For Running the BackEnd-Service in localhost

**Move to backend directory** : cd monolithic_backend/

Go to .env.dev (development environment) file :
1. Make sure to assign a MONGODB URI Link. You can generate your own cluster from [here](https://www.mongodb.com) 
2. Feel free to use your custom port


Download the node modules in each working directory using **npm install** 


**To run the project** : npm run dev


## For Running this service in ec2

Push this codebase to the created ec2 instance and run the same command as mentioned above in the working directory of folder

------ 

## For Running the FrontEnd-Service in localhost


**Move to frontend directory** : cd monolithic_frontend/

Download the node modules in each working directory using **npm install** 

**To run the project** : npm start (if root permissions are required, use **sudo**)


## For Running this service in ec2

Push this codebase to the created ec2 instance and run the same command as mentioned above in the working directory of folder

> In ec2, you can not directly run an application on PORT 80. Make sure to Setup an Nginx Reverse Proxy for running the frontend-service. (Refer [AWS Docs](https://aws.amazon.com/tutorials/setup-an-nginx-reverse-proxy/) [Stackoverflow](https://stackoverflow.com/questions/17413526/nginx-missing-sites-available-directory))


