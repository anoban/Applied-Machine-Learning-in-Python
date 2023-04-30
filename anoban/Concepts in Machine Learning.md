# ___Concepts in Machine Learning___
--------------

- Machine learning (Supervised Machine Learning) tasks can be categorized into 2 primary groups.
    - Classification tasks -> the target values are discrete classes.
    These are called classification problems and the function we learn is called a classifier.           
    e.g. Predict whether a monetary transaction is fraudulent or not.      
         Predict what English word an audio signal best associated to.
         
    - Regression tasks -> the trget values are continuous values.        
    e.g. The time it would take a care with a given set of specifications to acceletate to 230 mph speed.
    

## ___Supervised Machine Learning: Classification example___
-----------------

- We have a table of data. With one record per row. 

- This table consists of information about fruits, like diameter, weight, taste, price, colour, sugar content, pH etc... and a label.

- This label describes the fruit type, like banana, lemon, strawberry, apple .. etc.

- Once we train a classifier on the data availabe, (that is to make it make sense of the assocoation between the features and the labels) we can use the model to predict the fruit types on new features data.

- Supervised learning requires a labelled dataset to learn from. So, where does this training data comes from?

- Labelled training data is typically provided by humans. 

- When the training data is small and there are just a few labels, labels can be provided by the developer or researcher. But in the context of massive datasets, crowdsourcing platforms like Amazon Mechanical Turk or Crowd Flower can be used to find freelances who offer to label supplied items by hand, using human intelligence.

- These are examples of more explicit labels. We can also obtain implicit labels.

- An example of an implicit label is, when a search engine offers a set of web pages for a query, and the user returns from the first suggested webpage in 1 second but takes 4 minutes in the second suggestion, the engine may assume the second suggestion is more relevant to the query than the first one.

## ___Unsupervised Machine Learning: Classification example___

- In many cases, we only have training data without labels. This will involve discerning structure / patterns / relationships in the training data. This implies findng interesting clusters or groups within the data.

- Once we discover this structure or groups, that structure can be used to summarize the input data or to make visualizations.     

- For example if we have an e-commerce site, we might receive a diverse array of visitors. Some might be quick browser types just checking for any sales/discounts, or shopping addicts who browse and buy everything, or bots trying to scrape the page and even researchers trying to study the webpage/business dynamics.      
    
- These people will spend different amounts of time on the page, depending on their interests and how this page relates to their interests.

- We can then take the data, use an unsupervised model to identify these different groups. Then we can tailer our site's design to attract the type of visitors we need and ward off the ones that we do not need.

- Since, we do not know how many groups are out there and how they look like and we do not have any labelled examples, this problem is a good contender for unsupervised learning solutions.

- We can also detect abnormal activities/outliers. Suppose we have a web server, and we get request from a select set of IP addresses daily at high frequencies. This might pose a security risk to our servers. This behaviour may allude a potential cyber attacker's renaissance or a web scraping bot's activity or even a shopping addict's activity.

## ___Once we identify we can use ML to solve a problem, how do we go about solving it?___
-------------------------

1) How to __represent the learning problem__ in terms which the computer can understand.
    e.g. how to represent features in the training data.
    what type of models (classifiers / regressors) to use?
    
2) Decide on an __evaluation method__ that provides a quality assurance or accuracy score on how reasonable the predictions are!
    e.g. what criteria can be used to evaluate the fitness of predictions?
    how to distinguish a good classifier from a bad one?
    a good classifier will typically have a higher accuracy score.
    
3) Search for the __optimal classifier & optimal parameters for the selected classifier__ to maximize the accuracy of the predictions.

## ___Feature representation___

- Here we are concerned with how to structure the raw input data in a systematic way that a ML model could make sense of.

- Consider our learning sample (training data) consists of spam emails.         
    What features of the email can be provided to the model? perhaps a vector of tokens and their cognate frequencies in the email body.
  
- Consider an array of images -> a numeric matrix of pixels might be a good chioce.

- Consider a collection of fruits -> weight, diameter, colour, sugar content, pH, density etc..

- These attributes of the entities in the learning sample is called __features.__

- Features can be visualized easily in a tabular form.

- Data availabe for learning & predictions &rarr; __weight(g), diameter (mm), colour, sugar, content (mg/100g), pH, density__

- Labels (only available in the training data) &rarr; __fruit, type__


| weight(g) | diameter (mm) | colour | sugar content (mg/100g) | pH | density (g/mL) | fruit | origin |
| --------- | ------------- | ------ | ----------------------- | -- | ------ | ----- | ---- |
| 121 | 40 | red | 89 | 6.45 | 1.4 | apple | Australian |
| 65 | 39 | pink | 567 | 8.51 | 1.21 | Rambuttan | Sri Lankan |

- Identifying the important & informative features can be challenging as well. (Called feature engineering / feature extraction).

- In a tabular representation, each row represents a single data instance and each column represents a feature.

- The next step is choosing an appropriate algorithm/model for the learning process.

- Machine learning is often an iterative process. First we make a guess about which features to consider in the training, train the model, make predictions and evaluate how well the model performs.

- If there is room for improvement in terms of model performance, consider adding/removing some features, tuning certain parameters, repeat the learning & prediction steps, repeat the evaluation ... rinse and repeat until we get a satisfactory performance.

- This refining is very common in ML tasks.