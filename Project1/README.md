# Project1-Hosting-a-website-in-AWS-serverless-using-APIGateway-Lambda-DynamoDB

1. This website can take the customer information from front end and upload it to the database.
2. We are using below architecture to implement this website in AWS using serverless architecture.
   ![Architecture](https://github.com/user-attachments/assets/484cc307-69a9-450e-8e91-c70156832f93)

4. Create an IAM role for lambda with Lambda execution role and dynamoDB full access policy.
5. Create a lambda function and attch this IAM role to it.
6. Upload your website code onto lambda function and deploy it. The code contains get and post methods. Get method is to get customer info page and post method is to upload client filled information into dynamo db.
7. Create a dynamo DB table with default settings for now and keep it aside.
8. Create API in API gateway with 2 methods (GET, POST) and point it to your lambda function.
9. Now you can take the reference URL of your API and search it in browser.
10. You will be taken to your website, fill the information and submit the page.
11. Check your dynamo db table to see if the data is entred.
