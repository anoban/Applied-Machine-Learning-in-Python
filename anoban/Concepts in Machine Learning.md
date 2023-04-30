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

- We can then take the data, use an unsupervised model to 