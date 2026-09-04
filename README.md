# **loan-default-risk**
A machine learning pipeline designed to predict credit default risk using the UCI German Credit dataset. This project prioritizes a strict, leak-free methodology and business-cost optimization over standard accuracy metrics.

Goal:
Build a machine learning pipeline optimized to generate the lowest possible financial cost for loan approvals and rejections.

### Constructs 
> 1. Classing a good customer as bad. cost = 1
> 2. Classing a bad customer as good. cost = 5

read german.doc for more details from the UCI German Credit dataset

> Data splits into three

    > a. Training data
    > b. Validation data
    > c. Testing data

a. Training data to train the model to learn patterns to distinguish between applicants

b. Validation data to tune the model to get the lowest cost.

c. Test data to test the fine tuned model with a threshold to check for predictions, cost and accuracy. (Lowest cost is the best)

# **Model Selection** 

1. **Logistic Regression:** Using logistic regression here to split the applicants into classes 1 (Bad) and 2 (Good). Based on the provided data of each applicants in the training and validation data.

**Inference** : Based on the model's performance, we checked on the validation set, we have to choose the best threshold to predict the classes. Based on the confusion matrix we can clearly see that the best threshold is 0.1, in a range of 0.1 to 1.0 (0.1 intervals)

> *Applying this 0.1 threshold to the untouched Test Set resulted in 95 False Positives, 4 False Negatives, and a final business cost of 115.*
