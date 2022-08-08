# Fraud_Detection_AWS_SageMaker
This project is a fraud detection system that encorporates the use of XGBoost on credit card transactions to detect fraudulent ones. The Machine Learning algorithm has been developed and deployed using Amazon SageMaker. 

<!-----------------------> 

S3 bucket prefix to train the model is a specification. 
IAM Role to provide training and hosting access to data is also a specification. 
![image](https://user-images.githubusercontent.com/31934083/183363232-755081f5-a353-4432-bd80-a8f00066a650.png)



Steps: 

- Downloading the dataset from the internet into Amazon SageMaker.  

*Dataset*: (credit-card-transactions dataset): https://s3-us-west-2.amazonaws.com/sagemaker-e2e-solutions/fraud-detection/creditcardfraud.zip
### Note: The data is already normalized and standardized with unit standard deviation. 

Time: Number of seconds elapsed between this transaction and the first transaction in the dataset
V1-V28: Columns that have been transformed in order to protect user-sensitive information. 
Amount: The amount of money that has been incurred as a result of the transaction. 
Class: 0 or 1 (0 - Non-fraudulent, 1 - fraudulent). 

<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183359972-a8ada6d8-2a9b-44a8-90d4-b833f48d2a99.png">


- Investigating and transforming the data so that it can be fed into Amazon SageMaker Algorithms. 
![image](https://user-images.githubusercontent.com/31934083/183363682-7bb0cd78-c2e8-4b72-a259-b39c3cfa4590.png)

![image](https://user-images.githubusercontent.com/31934083/183363523-d5d3af26-b910-415c-bce8-9b15d84a0015.png)


- Estimating a model using the Gradient Boosted algorithm. 
<img width="1448" alt="Screen Shot 2022-08-08 at 5 16 26 pm" src="https://user-images.githubusercontent.com/31934083/183364313-b78cbbbe-0e19-4325-b679-c69927175b52.png">
<img width="1448" alt="image" src="https://user-images.githubusercontent.com/31934083/183364478-b05d9de8-03a2-461a-8b4a-30e8f8c7ee48.png">



 In the case of training data, it is necessary to provide the location of the XGBoost algorithm containers. 
 


- Evaluating the effectiveness of the model. 

![image](https://user-images.githubusercontent.com/31934083/183364169-e98e0243-16c8-4aac-a39b-68f59d7e3762.png)



From the figure, the accuracy of the model is 99.96% (Overall Predictions). 


AutoML is another option that can be used to train the model hyperparameters, which helps save time as well! 

![image](https://user-images.githubusercontent.com/31934083/183364096-12c47d0a-29de-433b-825d-207eaed1ec02.png)
