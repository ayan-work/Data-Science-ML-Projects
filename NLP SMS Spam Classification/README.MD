#                                                                 SMS Spam or Ham Classification

### Project Goal
Use the dataset to build a prediction model that will accurately classify which text are spam or ham(Legitimate).

### Data Source
The data used, is from [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php). Link: https://archive.ics.uci.edu/ml/datasets/sms+spam+collection

### Data Description
The data file contains multiple lines and each line consist of the text message and it's Label(Spam or Ham). Data is **unlabelled**.
Dataset consist of 5574 messages and 2 Columns

Initial Data:
![alt text](https://github.com/ayan-work/Data-Science-ML-Projects/blob/main/NLP%20SMS%20Spam%20Classification/Findings%20Images/Unlabelled%20data%20SMS.PNG)


### Findings

I have made two extra feature from the dataset i.e **Text length** and **Punctuation % in text** it helped the model with more features.

**Insights with Text length**
* **Spam:** These type of messages generally have the length varied from 130-170 words. The disribution left skewed. 
* **Ham:** These kind of messages have length varying from 30-100 words. 

Text Length Distribution boxplot:
![alt_text](https://github.com/ayan-work/Data-Science-ML-Projects/blob/main/NLP%20SMS%20Spam%20Classification/Findings%20Images/Text%20Length%20boxplot.png.png)

_So according to the boxplot distribution:_
* Ham messages's length have IQR(50% data) in range of 40-90 words. While it have it have 99.3% data in range of 5-175 words
* Spam messages's length have IQR(50% data) in range of 130-160 words. Its 99.3% data lies in range of 100-175 words

**Insights with punctuation percentage in text**

Punctuation percentage distribution:
![alt_text](https://github.com/ayan-work/Data-Science-ML-Projects/blob/main/NLP%20SMS%20Spam%20Classification/Findings%20Images/Text%20punctuation%20%25%20boxplot.png)

* **Spam:** Punctuation used in spam messages are comparetively less. 99.3% data lies in range of 0-12%. while the median is around 4%. 50% data have 3-5% punctuation
* **Ham:** Punctuations used in ham messages is large. 99.3% data are in range of 0-16%. while 50% data have 3-8% punctuations. Median is around 5%.

### Conclusion

* I have achieved an overall accuracy of 97% by implementing Random Forest Classifier modeled with Tfidf Vectorizer.
* For model evaluation I have used AUC-ROC Curve, and got AUC-ROC score of 99.3%

AUC-ROC Curve:
![alt_text](https://github.com/ayan-work/Data-Science-ML-Projects/blob/main/NLP%20SMS%20Spam%20Classification/Findings%20Images/AUC-ROC%20Curve%20for%20SMS%20spam.png)
