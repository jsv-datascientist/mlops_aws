# mlops_aws
Creating a MLOPS in AWS environment


# 1. First step is the set up the IAM Identity Center
   
Lets say we have a developer group of 3 people and a devops engineer. 
Let the rootuser be devops-root@abc.com
and one of the developer be dev1@abc.com
We create different AWS accounts for above people. To maintain the permissions it is recommanded to use IAM Identity Center 

Go to AWS, login with root user like ( devops-root@abc.com) and enable the IAM Identity Center and select teh proper region.
![image](https://github.com/user-attachments/assets/f2010fbf-c735-42bd-8a8a-68b0d0ed6bae)

## 1.1 Create the Permissions 
Click on the Permission sets and select the AdmnistratorAccess

![image](https://github.com/user-attachments/assets/b98b1159-9602-479e-a3ed-9a4d2f143765)

Select the duration based on  the need and click next to have the permission set 

![image](https://github.com/user-attachments/assets/c3693079-8e92-4a57-a10f-e86cf7f9ede7)

   
## 1.2 Create tge Groups 
On the left side , click on Groups and create the group. It could be Admin, Devs, DevOps etc

![image](https://github.com/user-attachments/assets/04e69a03-a988-4e1c-97d4-478aa0028576)

## 1.3 Create the AWS Account 


Click on the AWS accounts and select the root user 

![image](https://github.com/user-attachments/assets/c72650c5-43f8-45d7-ab09-e0af9df5b9b1)

Click on Assign users and group


![image](https://github.com/user-attachments/assets/464131aa-bdfd-45f7-8b66-2f74e633a141)

click on add users and follow the name 
Note: Make a note of the username entered here and the email id. This is needed for login each time we need access
![image](https://github.com/user-attachments/assets/cc1300e4-097e-4914-881a-74d5de02bd4d)


![image](https://github.com/user-attachments/assets/64a0f5d1-eab2-49ff-9ca0-e924175e9a43)


Select user , groups, permissions and set up the process. 

![image](https://github.com/user-attachments/assets/0d3f85d1-b3ae-4bf1-b89c-8c0aa83f09ff)

you will get an email for accepting the invitation. Follow the process and save it. 
The url present here in the IAM instance will be used by all users to access it. 

![image](https://github.com/user-attachments/assets/cfdca16b-3084-40ea-87b0-ee382d03edcc)




# 2. AWS Vault 

Open the IAM Identity Center URL for the Developer1 using username and password set up in previous process. 
You will find the below 
![image](https://github.com/user-attachments/assets/1fedb4ca-c26f-4511-9bac-ee56d6be1dfd)

Click on the access key and take a note of the credentials 
![image](https://github.com/user-attachments/assets/611194c5-50f5-4e07-87a6-017311ead82e)


Press Enter , it will popup the screen to validate 
![image](https://github.com/user-attachments/assets/bac61dc9-a680-4722-a34c-90385a06e3e8)


![image](https://github.com/user-attachments/assets/b9f42a7f-4320-4215-9a33-8853d204a76f)


![image](https://github.com/user-attachments/assets/eb2504a5-7560-4649-9a65-1cd673e8f13b)


![image](https://github.com/user-attachments/assets/9d01707b-5249-4436-ac9c-40ae134c5ddc)

![image](https://github.com/user-attachments/assets/826e2d7a-85a1-4f49-9264-ef5c08829fb8)

.aws directory will be created 
![image](https://github.com/user-attachments/assets/d2c5b896-1699-49c9-be96-92babb6b0234)

![image](https://github.com/user-attachments/assets/c75caf9a-db74-47d1-9288-442eed2ced40)

Run below command in .aws folder and enter password, now we are connected to our environment. 

![image](https://github.com/user-attachments/assets/a8733452-05f3-4a73-a05d-cd8af9c21539)















