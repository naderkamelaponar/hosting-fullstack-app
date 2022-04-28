# AWS Hosting Udagram App

## Dependencies 

- Node v14.15.1 (LTS) or more recent
- npm 6.14.8 (LTS) or more recent
- AWS CLI v2
- A RDS database running Postgres.
- Elastic beanstalk  to run the API
- A S3 bucket for hosting uploaded pictures.


## AWS 
### AWS Infrastructure
### - S3 Bucket 
 **S3 Bucket** is for the  'Udagram front-end' [http://udagram-bucket-123-4567-1890.s3-website-us-east-1.amazonaws.com](http://udagram-bucket-123-4567-1890.s3-website-us-east-1.amazonaws.com)

1. Receives Requests from the user And then send it to **Elastic Beanstalk**
2. Sends Back Responses from the **Elastic Beanstalk** to the User
### - Elastic Beanstalk
**Elastic Beanstalk** is for the  'Udagram Api' [http://udagram-app-dev.eba-mzghj4hc.us-east-1.elasticbeanstalk.com/](http://udagram-app-dev.eba-mzghj4hc.us-east-1.elasticbeanstalk.com/) 
1. Receives a Requests  from the **S3 Buckets**
2. Sends Queries to the **RDS Postgres DB**
3. Sends Responses to the **Elastic Beanstalk**
### - RDS Postgres DB
**RDS Postgres DB** 'Udagram Database' udagram.c1g1hzuv0at4.us-east-1.rds.amazonaws.com
1. Receives Queries from **Elastic Beanstalk**
2. Sends Data to **Elastic Beanstalk**
### - AWS Diagram
![aws diagram](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/aws-diagram.png)

  
## Pipeline
### Pipeline Infrastructure 
### - GitHub 
When the Developer Push a code to **GitHub** 
It will trigger the `.circleci/config.yml` file.
### - Circle Ci 
The **Circle Ci** Service will execute `.circleci/config.yml` to do the following Jobs :

1. Prepare the Environment Variables which Will be passed to the AWS,EB And the udagram-api
2. Install the Pipeline Dependencies 
which well be 

- `node: circleci/node@5.0.2
    browser-tools: circleci/browser-tools@1.2.3
    aws-cli: circleci/aws-cli@3.1.0
    eb: circleci/aws-elastic-beanstalk@1.0.0`

3. It will run the predefined Jobs to Test And Deploy the udagram-frontend and udagram-api

![Circle Ci Steps](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/circleCi-steps-1.jpg)
--
![Circle Ci Steps](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/circleCi-steps-2.jpg)
--
[Back](https://github.com/naderkamelaponar/hosting-fullstack-app)
## Circle Ci  Environments
![Circle Ci  Environments](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/circleCi-Env-Vars.jpg)
--
![Circle Ci  Environments](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/circleCi-Env-Vars-1.jpg)
--
[Back](https://github.com/naderkamelaponar/hosting-fullstack-app)
## AWS Resources Health
![eb health](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/eb-health.jpg)
--
![RDS DB](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/rds-db.jpg)
--
![RDS DB](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/rds-db-1.jpg)
--
![S3 Bucket](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/s3-bucket.jpg)
--
![S3 Bucket](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/s3-bucket-1.jpg)
--
![S3 Bucket](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/s3-bucket-2.jpg)
--
[Back](https://github.com/naderkamelaponar/hosting-fullstack-app)
## Pix 4 the Reviewer
![pic from console user](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/pic-from-console-user.jpg)
--
![Billing Dashboard](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/billing-dashboard.jpg)
--
[Back](https://github.com/naderkamelaponar/hosting-fullstack-app)   