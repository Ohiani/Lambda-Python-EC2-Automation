# LAMBDA-PYTHON EC2 AUTOMATION

# eC2 start and stop automation using lambda functions and Aws EventBridge
In this project, we will be building a lambda function to start and stop a set of ec2 instances at a specific time and also send event notifications incase of failure. The tools we would be using to achieve this goals are 
- Lambda
- python
- AWS Eventbridge 
- SNS


## Starting Off AWS Project

- Create a set of ec2 instances on your AWS account
- Add same tags to all the ec2 instances you would like to automate
![](./Screenshot%202023-11-24%20151218.png)

![](./Screenshot%202023-11-26%20113219.png)

## Setting Up Your Lambda Functions And EventBridge

1. Create lambda function

![](./Screenshot%202023-11-24%20151653.png)

![](./Screenshot%202023-11-24%20152417.png)

2. Attach ec2 permission to the new IAM role created by the lambda function

![](./Screenshot%202023-11-24%20153720.png)

3. Edit your function code
![](./Screenshot%202023-11-24%20210051.png)
   

4. Test output

![](./Screenshot%202023-11-24%20210037.png)

![](./Screenshot%202023-11-26%20114616.png)

5. Create an eventbridge schedule to stop the instance daily at 7pm WAT
   
![](./Screenshot%202023-11-26%20105417.png)

![](./Screenshot%202023-11-26%20110239.png)

![](./Screenshot%202023-11-26%20110315.png)

6. Create an SNS notification to send a notification to an email whenever a failure occures
   
![](./Screenshot%202023-11-26%20110923.png)

7. Repeat the above test for the startec2instance lambda function but change the python code 
![](./Screenshot%202023-11-26%20104417.png)

![](./Screenshot%202023-11-26%20115708.png)


