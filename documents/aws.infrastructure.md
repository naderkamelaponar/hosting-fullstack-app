# AWS Infrastructure

## Dependencies 
- A S3 bucket to host the front end and to store the uploaded pictures.
- Elastic Beanstalk  to run the API
- A RDS database running Postgres.
### - S3 Bucket 
 **S3 Bucket** is for the  'Udagram front-end' [http://udagram-bucket-123-4567-1890.s3-website-us-east-1.amazonaws.com](http://udagram-bucket-123-4567-1890.s3-website-us-east-1.amazonaws.com)
#### How come the S3 Bucket Work ?
1. Receives Requests from the user And then send it to **Elastic Beanstalk**
2. Sends Back Responses from the **Elastic Beanstalk** to the User 
3. Saves the Uploaded pictures .
### - Elastic Beanstalk
**Elastic Beanstalk** is for the  'Udagram Api' [http://udagram-app-dev.eba-mzghj4hc.us-east-1.elasticbeanstalk.com/](http://udagram-app-dev.eba-mzghj4hc.us-east-1.elasticbeanstalk.com/) 
#### How come the Elastic Beanstalk Work ?
1. Receives a Requests  from the **S3 Buckets**
2. Sends Queries to the **RDS Postgres DB**
3. Sends Responses to the **Elastic Beanstalk**
### - RDS Postgres DB
**RDS Postgres DB** 'Udagram Database' udagram.c1g1hzuv0at4.us-east-1.rds.amazonaws.com
#### How come the RDS Postgres DB Work ?
1. Receives Queries from **Elastic Beanstalk**
2. Sends Data to **Elastic Beanstalk**
## Environment Variables
### Create Variables that will receive the Values From the Pipeline to run the Deployed Api App
### Set the  Variables to the Elastic Beanstalk
- `AWS_ACCESS_KEY_ID <AWS_ACCESS_KEY_ID>`
- `AWS_DEFAULT_REGION <AWS_DEFAULT_REGION>`
- `AWS_SECRET_ACCESS_KEY  <AWS_SECRET_ACCESS_KEY>`
- `POSTGRES_DB <OSTGRES_DB>`
- `POSTGRES_HOST <POSTGRES_HOST>`
- `POSTGRES_USERNAME <POSTGRES_USERNAME>`
- `JWT_SECRET  <JWT_SECRET>`
- `PEPPER <PEPPER>`
- `SALT <SALT>`
###  AWS Diagram
![aws diagram](https://raw.githubusercontent.com/naderkamelaponar/hosting-fullstack-app/main/documents/images/aws-diagram.png)
## AWS Resources Health  Screenshots 
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
[Back](https://github.com/naderkamelaponar/hosting-fullstack-app/blob/main/documents/doucments.md)