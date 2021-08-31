# consumer-complaint-classification

DSE Capstone Project

                                        Project Details
Overview:
Banks provide a number of services to their customers and as a result of this they face a 
variety of challenges on a daily basis. These challenges may range from issues related to, but not 
limited to, customer credit and debit, education loan, customer churning, mortgages, and daily 
transactions.

Over the past few years’ banks have increased their social presence. This has led them to 
receive a large number of complaints from various sources such as Twitter, Facebook, and the 
Consumer Financial Protection Bureau. If The bank fails to solve or even address the complaints of 
its customers, they will be greatly disappointed by its services. This would lead to a diminished brand 
image and in-turn affect business. Manually responding to each and every complaint in time is not 
feasible and an extremely tedious task as every complaint has to be read and routed to the concerned 
department. Banks are looking at ways to reduce this manual effort and improve response time. In 
this project we are trying to leverage the large amount of unstructured data that banks receive to 
provide one such solution to this problem.

Business problem statement (GOALS):

What would you achieve by this project?
From a business perspective, it would help the bank greatly reduce response time of 
complaints, help develop policies to improve customer satisfaction and help regulate consumer 
financial products and service.

How Would this help the business or client?
We will be trying to make use of machine learning and text classification to build a classifier
that helps segregate complaints and assign the complaints to the concerned department.
What is the current scope and suggest an extension to the scope?
Currently we are looking to automate the process of assigning complaints for one given 
Product to the concerned sub-department for a couple of major banks. We could further extend the 
scope by trying to build a similar model for multiple products of various banks.
Limitation of project
1. Our model is specific to one particular product and cannot be applied to a different product, 
i.e., it is not generalized model
2. If new features are added to the product and complaints are issued on those features, our 
model is not dynamic enough to understand and provide accurate results for complaints 
pertaining to the new feature

Topic survey in brief:
This database is a collection of complaints about consumer financial products and services 
that will be sent to companies for response by Consumer Financial Protection Bureau. Complaints 
are published after the company responds, confirming a commercial relationship with the consumer, 
or after 15 days, whichever comes first. 
Existing Solutions have only emphasized on initial data processing and exploratory data 
analysis so we emphasis more on build models that can provide insights and add value.
Critical assessment of topic survey:
The one idea behind the project is to address a way of using the unstructured data for decision making. 
The selected business data is made sure the consumer complaint narrative is identified for a particular 
product and particular issue type and the narrative in the dataset has been filtered to identifying the 
removing stop words, quotations, whitespace, punctuation and numbers.
Text data analytics is a component on NLP to identify the above-mentioned filter content and 
categorize it. The text data used to solve complaint narrative of a particular product and issue type of 
bank can similarly implemented to other areas, can be used for structured data for faster decision 
making

Methodology to be followed:
1. Business Understanding:
This is the first step. It begins with the understanding of the business problem statement that 
we would analyze which forms the basis of an effective solution to the business problem.

2. Data Understanding:
In this step we understand the data using visualization techniques using libraries like seaborn, 
matplotlib and Plotly and get descriptive statistics using NumPy and Pandas libraries by which 
we understand different attributes, assess its quality, and obtain initial overview about the data.

3. Data Preparations and EDA:
After understanding the data, we start performing data pre-processing as a part of data 
cleaning, data transformation using suitable data encoding into more useful variables and handle 
outliers or skewness in the data.

4. Modeling: 
From the prepared data, we divide the data into training and testing. The training data is used 
for model building and test this model on the testing data to get the accuracy. The modeling 
process involves using sentiment analysis to achieve the target variable.
DSE Capstone Project 
Guidelines
 
 Issue Classification
The dataset has a text field that has consumer complaint narrative, customer id to identify uniquely 
and text field that has customer review.
Step 4.1: 
Identifying the topic: Narrow down the problem statement to bank, product and number of issue types
Step 4.2:
Tokenization:
Identify keywords specific to the complaint. These keywords must be exclusive. Build list based on 
the primary keywords, secondary keyword assigned to topic, subtopic.
egg: Topic: Mortgage, Keywords: loan, foreclosure, escrow amount
Word tokenization splits the words into individual words based on certain delimiter.
Step 4.3:
Stop word filtering:
With python we have several NLP libraries to remove stop words from the complaint narrative e.g.
NLTK, SpaCy etc. To remove the stop words, we divide the text into words and remove the word 
that exists in the library
Step 4.4:
Negation Handling:
Negative words are not used to analyze and they carry no meaning. We can avoid them by not 
applying sentiment or by removing them entirely
Step 4.5:
Stemming:
Stemming is a method of removing the suffix of the word and bringing it to a base word. Stemming 
reduces the number of computations required, dimensionality of data. We can do stemming in NLP 
using libraries such as Porter Stemming, Snowball Stemmer, etc.
Step 4.6:
Classification:
Each customer id is mapped to topic / subtopic. the model built will use the functionality of the 
packages (NLTK) to identify the sentiment. 
DSE Capstone Project 
Guidelines

5. Evaluation:
We evaluate the quality of the model and verify that the business problem is handled in a 
complete and adequate manner.


Input Sample Data:
Product Bank Name: Issue Complaint Narrative

Credit card:  Wells Fargo 
& Company

Cosumer Complaint Narrative :

Billing disputes I purchased a refrigerator and a cooking range from XXXX in 
XXXX, AZ around XX/XX/XXXX which was charged on a Wells 
Fargo credit card issued through the retailer. The terms of the 
finance was Zero interest if full purchase amount was paid within 
12 months of purchase which was XX/XX/XXXX ( " Expiration Date 
'' ). The total purchase price for both appliances was {$2700.00}. 
These appliances were purchased for my new house where I did 
n't move until XX/XX/XXXX. Due to the various activities involving 
the move and due to the issues with mail forwarding, I was 
behind in attending to my mail. As a result I did n't make the 
payment for the first two cycles on time but did pay them a few 
days later by phone along with late fees of about {$25.00} each 
time. I was told that my account is now current and as long as I 
made the full remaining balance on my account by the Expiration 
Date, I would no longer pay any interest. In order to ensure no 
more delays, I scheduled regular payments on my bank 's bill pay 
system so that payment gets sent each month on time and the 
full remaining balance is paid before the Expiration Date. Below 
is the schedule of all payments made : Date AmountXX/XX/XXXX 
$ XXXXXX/XX/XXXX $ XXXXXX/XX/XXXX $ XXXXXX/XX/XXXX $ 
XXXXXX/XX/XXXX $ XXXXXX/XX/XXXX $ XXXXXX/XX/XXXX $ 
XXXXXX/XX/XXXX $ XXXXXX/XX/XXXX $ XXXXXX/XX/XXXX $ 
XXXXXX/XX/XXXX $ XXXXXX/XX/XXXX $ XXXXTotal Paid $ 
XXXXPurchase Amt. $ XXXXFees Paid $ ( XXXX ) Wells Fargo 
however kept carrying a balance of {$10.00} on my account and 
then charged me interest on it even after the last payment was 
made on XX/XX/XXXX. When I called them, they corrected the 
mistake but also closed my account and reported it to the Credit 
Bureaus as late payment for the month of XX/XX/XXXX. While I 
made the full payment of {$2700.00} before expiration date and 
paid them late fees for the first couple missed payments, they 
have taken the wrongful action of closing my account and making 
derogatory submission to the credit bureaus, when the 
underlying cause of this was **their mistake** of having left over 
fees on my account. 

References:
1) https://www.datacamp.com/community/tutorials/simplifying-sentiment-analysis-python
2) https://ieeexplore.ieee.org/document/8487638
3) https://medium.com/@tomyuz/a-sentiment-analysis-approach-to-predicting-stock-returnsd5ca8b75a42
4) https://saurabhraj5162.medium.com/case-study-customer-complaints-analysis-ml-modeltraining-4a2583d7a073
5) https://reader.elsevier.com/reader/sd/pii/S187705091932126X?token=963301BABD9B6A2A43
2AFF1889399A24027C4E4B7F07C57C1A69A3458DA4488C512803479E38F5053AC122D83
47119C8&originRegion=eu-west-1&originCreation=20210808073828
6) https://www.analyticsvidhya.com/blog/2021/06/nlp-sentiment-analysis/
7) https://monkeylearn.com/sentiment-analysis/
8) https://www.kdnuggets.com/2018/08/emotion-sentiment-analysis-practitioners-guide-nlp-5.html
9) https://www2.deloitte.com/content/dam/Deloitte/us/Documents/financial-services/us-fsi-cfpbconsumer-complaint-database-091913.pdf
10) https://esource.dbs.ie/bitstream/handle/10788/4224/msc_shivaprasad_vm_2020.pdf?sequence=
1&isAllowed=y
11) https://towardsdatascience.com/detecting-bad-customer-reviews-with-nlp-d8b36134dc7e
DSE Capstone Project 
Guidelines
Notes For Project Team:
Original owner of data Consumer Financial Protection Bureau
Data set information Classifying customer complaints for a given 
product and assigning the complaints to the 
concerned sub-department for several major 
banks
Any past relevant articles using the dataset Case study: Customer Complaints Analysis
& ML model training
Reference https://saurabhraj5162.medium.com/case-studycustomer-complaints-analysis-ml-modeltraining-4a2583d7a073
Link to web page https://www.consumerfinance.gov/dataresearch/consumer-complaints/
                                                                  
                                                                  ** THE END **
