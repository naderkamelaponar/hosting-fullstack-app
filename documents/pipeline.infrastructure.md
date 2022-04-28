
## Pipeline Infrastructure 
## Dependencies 
    node: circleci/node@5.0.2
    browser-tools: circleci/browser-tools@1.2.3
    aws-cli: circleci/aws-cli@3.1.0
    eb: circleci/aws-elastic-beanstalk@1.0.0

## Environment Variables
### Create Variables And Set the Values that will be used  to access the AWS and  to run the Deployed Api App
### Set the  Variables to the Pipeline Service
- `AWS_ACCESS_KEY_ID <AWS_ACCESS_KEY_ID>`
- `AWS_DEFAULT_REGION <AWS_DEFAULT_REGION>`
- `AWS_SECRET_ACCESS_KEY  <AWS_SECRET_ACCESS_KEY>`
- `POSTGRES_DB <OSTGRES_DB>`
- `POSTGRES_HOST <POSTGRES_HOST>`
- `POSTGRES_USERNAME <POSTGRES_USERNAME>`
- `JWT_SECRET  <JWT_SECRET>`
- `PEPPER <PEPPER>`
- `SALT <SALT>`

## How it works ?
### - GitHub 
When the Developer Push a code to **GitHub** 
It will trigger the `.circleci/config.yml` file.
### - Circle Ci 
The **Circle Ci** Service will execute `.circleci/config.yml` to do the following Jobs :

1. Prepare the Environment Variables which Will be passed to the AWS,EB And the udagram-api
2. Install the Pipeline Dependencies 
3. It will run the predefined Jobs to Test And Deploy the udagram-frontend and udagram-api
--
## Circle Ci  Environments
![Circle Ci  Environments](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/circleCi-Env-Vars.jpg)
--
![Circle Ci  Environments](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/circleCi-Env-Vars-1.jpg)
--
## Circle Ci  Steps
![Circle Ci Steps](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/circleCi-steps-1.jpg)
--
![Circle Ci Steps](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/circleCi-steps-2.jpg)
--
[Back](https://github.com/naderkamelaponar/hosting-fullstack-app/blob/main/documents/doucments.md)

