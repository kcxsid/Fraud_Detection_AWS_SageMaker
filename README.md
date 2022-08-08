# Fraud_Detection_AWS_SageMaker
This project is a fraud detection system that encorporates the use of XGBoost on credit card transactions to detect fraudulent ones. The Machine Learning algorithm has been developed and deployed using Amazon SageMaker. 

<!-----------------------> 

S3 bucket prefix to train the model is a specification. 
IAM Role to provide training and hosting access to data is also a specification. 
<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183360648-9a37dda3-41a1-4c3f-ad16-b6de93345fd1.png">



Steps: 

- Downloading the dataset from the internet into Amazon SageMaker.  

*Dataset*: (credit-card-transactions dataset): https://s3-us-west-2.amazonaws.com/sagemaker-e2e-solutions/fraud-detection/creditcardfraud.zip
### Note: The data is already normalized and standardized. 

Time: Number of seconds elapsed between this transaction and the first transaction in the dataset
V1-V28: Columns that have been transformed in order to protect user-sensitive information. 
Amount: The amount of money that has been incurred as a result of the transaction. 
Class: 0 or 1 (0 - Non-fraudulent, 1 - fraudulent). 

<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183359972-a8ada6d8-2a9b-44a8-90d4-b833f48d2a99.png">


- Investigating and transforming the data so that it can be fed into Amazon SageMaker Algorithms. 
<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183360174-0ae085f6-3214-4c35-93ff-0145cb24b541.png">
<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183360174-0ae085f6-3214-4c35-93ff-0145cb24b541.png">


- Estimating a model using the Gradient Boosted algorithm. 

<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183360174-0ae085f6-3214-4c35-93ff-0145cb24b541.png">
<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183360174-0ae085f6-3214-4c35-93ff-0145cb24b541.png">

 In the case of training data, it is necessary to provide the location of the XGBoost algorithm containers. 
 
 <img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183360174-0ae085f6-3214-4c35-93ff-0145cb24b541.png">


- Evaluating the effectiveness of the model. 

<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183360174-0ae085f6-3214-4c35-93ff-0145cb24b541.png">

From the figure, the accuracy of the model is 99.96% of overall predictions. 


AutoML is another option that can be used to train the model hyperparameters, which helps save time as well! 

<img width="1533" alt="image" src="https://user-images.githubusercontent.com/31934083/183360174-0ae085f6-3214-4c35-93ff-0145cb24b541.png">

