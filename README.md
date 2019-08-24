# Starbucks EDA and prediction model
- This is one of the projects of my Udacity Machine Learning NanoDegree Program

## Introduction
Our task is to combine transaction, demographic and offer data to determine which demographic groups respond best to which offer type. This data set is a simplified version of the real Starbucks app because the underlying simulator only has one product whereas Starbucks actually sells dozens of products.<br/>

## Dataset
The data is contained in three files:

`portfolio.json` - containing offer ids and meta data about each offer (duration, type, etc.)
`profile.json` - demographic data for each customer
`transcript.json` - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

**portfolio.json**
* id (string) - offer id
* offer_type (string) - type of offer ie BOGO, discount, informational
* difficulty (int) - minimum required spend to complete an offer
* reward (int) - reward given for completing an offer
* duration (int) - time for offer to be open, in days
* channels (list of strings)

**profile.json** 
* age (int) - age of the customer 
* became_member_on (int) - date when customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

**transcript.json**
* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours since start of test. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record

## My Objective
-	Get basic stat of our app users, including their age, income distribution
-	Determine which demographic group will likely to purchase with and without advertisement 
-	Determine which offer type is most impactful
-	Build a binary classifier to predict whether a customer will complete the offer 

## Evaluation Metrics
Validation accuracy, precision score, recall score and F1 score will be used to evaluate the model performance

## Package required
- pandas
- seaborn
- sklearn
- Keras
