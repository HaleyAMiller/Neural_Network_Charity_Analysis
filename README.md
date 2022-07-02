# Neural Network Charity Analysis

## Alphabet Soup Analysis Overview
#### The non-profit organization Alphabet Soup that raises and donates money to organizations focused on improving the environment, enhancing peoples’ well-being, and connecting people from across the globe. The organizations that Alphabet Soup works with vary from small groups to large foundations with an abundance of variability between the groups served. With previous data from over 34,000 organizations, a team at Alphabet Soup is looking to create a model that can accurately predict the success of organizations. To do this, machine learning was utilized, and several neural networks were created to analyze, train, and test the data provided. As the results from this analysis did not yield ideal results, more techniques will need to be utilized to create an effective model.

## Resources Utilized
##### Data Source: charity_data.csv

##### Software: Python 3.7.6; Anaconda 4.10.3; 


## Alphabet Soup Analysis Results
#### Data Preprocessing 
* As the aim of the models is to accurately predict whether or not organizations are successful in their use of Alphabet Soup funding, the target of this analysis was the IS_SUCCESSFUL column.
* The features of the analysis were APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.
* Subsequently as EIN and NAME only served as identifiers to the data and were not the target or features of the model, they were removed before creating the models.

#### Compiling, Training, and Evaluating the Models
* The first model created was a deep-learning neural network with two hidden layers that consisted of 80 neurons and 30 neurons respectively. Both hidden layers utilized the “relu” activation function in order to classify the data.
* The ideal performance of the model was 75% accuracy, however this model did not meet that metric. Please see the image below for the loss metric and accuracy score calculated to the first model.

![1st model](https://user-images.githubusercontent.com/99554642/177010915-39c8f24a-bb3b-4415-8d0c-377392a9422d.png)


* To improve the accuracy and loss metric of this model, three strategies were utilized. The first strategy attempted was to increase neurons to the second hidden layer. There were 20 neurons added to the second hidden layer to better classify the data, however this did not impact the model’s performance.
* The second strategy utilized was adding another hidden layer and decreasing the epochs. A third hidden layer was added with 10 neurons and the epochs were decreased to 50 epochs. Similarly to the first attempt to optimize the model, the second attempt did not have a significant effect on the model’s performance.
* The final strategy to improve the model was changing the activation function of the first hidden layer to a sigmoid. The model’s goal was to classify the data into a binary classification system so the sigmoid function was added to do so early on in the neural network. Unfortunately, this also did not improve the performance of the model. 


Below are the three additional strategies utilized and their resulting loss metric and accuracy.

![2nd Model](https://user-images.githubusercontent.com/99554642/177010924-804c17af-9379-468e-90bc-fbbe3e2555b2.png)

    ^ Adding additional neurons

![3rd Model](https://user-images.githubusercontent.com/99554642/177010933-3d6d7cb6-ebf1-4924-b0fd-2c74f316452e.png)

    ^ Adding an additonal layer/changing epochs

![4th Model](https://user-images.githubusercontent.com/99554642/177010937-54bbad20-9724-4cc6-8522-b4ec0f877d42.png)

    ^ Changing the activation function


## Alphabet Soup Analysis Summary
Each time the model was ran, even with the adjustments to the model, it yielded results with a loss metric of about .55 and an accuracy of about .72. These are not preferable for a functioning model to predict the success of fundraising for organizations as there is a large margin for error within the accuracy as well as a large amount of data being lost by running the deep-learning neural network. Neither of these factors are ideal for Alphabet Soup’s purposes.

There are two additional options to consider for Alphabet Soup moving forward. The team can choose to attempt another deep-learning neural network but with the keras tuner library from tensorflow. Utilizing this approach allows the models to automatically adjust the parameters and hyperparameters of the model to find the best model available in regard to a chosen metric; for Alphabet Soup, this would be accuracy. Another option for Alphabet Soup is to use supervised machine learning instead of a neural network as the goal for the team is to create a model that fits data into a known classification system (successful and not successful). 
