<h1 align="center">Vinuth Project 2</h1>

___

# Project Description
In this assignment we will be discussing regrading the Housing and comes the part where we earn or establish a business for our living sustenance so we wanted to check on the details related to business licenses and get some inputs from it. I got my datasets from website [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/business-licences-2013-to-2024/information/?disjunctive.status)
## Project Title: Understanding Business License Information
The primary goal here is to conduct a descriptive analysis of the yearly trends in business License based on the datasets taken from [City of Vancouver Open Data Portal](City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/business-licences-2013-to-2024/information/?disjunctive.status)). The goal is to identify the percentage of business Licenses over time, which can help inform operational strategies for this license services, improve response times, and increase the licenses for their respective businesses.
## Project Objective:
* Business Licenses have become crucial part of our lives.
* I decided this will be my dataset to get information related to  business Licenses  in city of Vancouver.
* For the DAP design there are close to 13 steps. Am going to define and describe all these steps below.
There is one  datasets which i will be using here.
* The  dataset is **"Issued Business License"**, it contains information on issued business license, with columns such as:
  * [Cummulative-business-licences-2024.xlsx](https://github.com/user-attachments/files/17004732/Cummulative-business-licences-2024.xlsx)
## Methodology:
* The process of DAP designing and implementation is complex.
* This involves 3 different steps. I will be explaining on these steps in detail below:
### Step 15: Data Protection
* This **Data Protection** entails preventing unauthorised access, misuse, or breaches of sensitive data.
* It is essential when working with datasets that might contain internal records or the private information of pet owners.
* To do this, we are generating KMS keys for the S3 buckets' data encryption and decryption.<br>
![fig06](https://github.com/user-attachments/assets/1abd780f-2b76-490e-823f-4a7b6fa238be)
* My newly created KMS key information is displayed in the image above. 
* In addition, I'm using the KMS key I made for my S3 bucket and S3 backup bucket to enable bucket versioning and encrypt data.<br>
![fig07](https://github.com/user-attachments/assets/63cdc595-8714-4858-a15a-c343d8f0d5b9)
* The information about my S3 bucket's properties is displayed in the images above.<br>
![fig08](https://github.com/user-attachments/assets/6589bcc9-703e-4df8-bf89-36be3c5f5535)
* The details of my S3 backup bucket's properties are displayed in the images above.
* I am mirroring my S3 bucket with another bucket in order to configure the backup option.
![fig09](https://github.com/user-attachments/assets/2d3ec253-38ec-4f70-a579-40df3f8b686e)
* The above image shows my replication information.
### Step 16: Data Governance
* The term "data governance" describes the guidelines, norms, and procedures for handling and utilising data in a way that complies with legal requirements as well as organisational objectives.
* It guarantees the security, integrity, and quality of data throughout its entire lifecycle.
* To protect sensitive data, I am first creating a Trusted folder where I can store data that has been masked.
* The created Trusted folder can be seen in the image above.
* I then develop an ETL to transform the accessible raw data, utilising ETL to locate and conceal sensitive data.
* The ETL pipeline for storing reliable information derived from raw data is depicted in the above image.
* After that, I store the data that was obtained from the ETL in the trusted folder.
* The above image shows the resultant information stored as csv file in trusted folder.
### Step 17: Data Monitoring
* To maintain data integrity, identify possible breaches, and assure compliance with governance policies, data monitoring entails continuously tracking data usage and access.
* The "**AWS CloudWatch**" service will be used in this instance to build a dashboard tailored to our requirements.
* 
* The AWS CloudWatch dashboard is seen in the above image.
* 
* After that, I use the "**AWS CloudTrail**" service to create a user activity trail so that I can monitor user behaviour for any abnormalities.
* 
* The cloud trail made to monitor user activity is depicted in the image above. The information about the cloud trail saved in S3 is shown in the image above.
