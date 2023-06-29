# Deep Learning Model: Sentiment Analysis of IMDB-Movie-Reviews

## About:
Attempt to build a reliable Deep Learning model that can predict the correct sentiment for IMBD movie reviews. The Neutral Network model was constructed using 8000 IMDB movie reviews. The raw review data was preprocessed to ensure data quality, involving parsing HTML content with BeautifulSoup, removing stop words, non-alphabetic words, and punctuation, and applying the Snowball Stemmer. The features were extracted from the preprocessed movie reviews using the bag-of-words method. Additionally, hyperparameters for the Neural Network architecture, such as the number of layers, neurons, and activation functions, were carefully selected. Specific model parameters, including the optimizer, learning rate, loss function, metric, and number of epochs, were also chosen.<br>
**Result: training score of 87% and testing score of 84%.**

## Code is Divided Into The Following Section:
* ### Collecting Data:
    * Reads the IMDB movie reviews data stored in the CSV file into a pandas DataFrame.
    * Selected 8000 reviews since the dataset was quite large and consisted of 25,000 reviews.
    * Checked if the dataset labels were balanced.
    * Separated main Dataframe into two: reviews (features) and sentiment (labels).
* ### PreProcessing The Data For ML:
   * Used BeautifulSoup to parse the HTML content from the raw review data and collect the text content.
   * Tokenized the text content then:
      * Removed punctuation
      * Removed stopwords
      * Removed non-alphabetic words
      * Used SnowBallStemmer to stem each word
   * Joined the list of preprocessed words   
* ### Prepare Data For Neutral Network:
   * Used the bag of words method to extract the features from the preprocessed movie reviews.
   * Used the label encoder method to add numeric values for the string labels (0=negative, 1=positive).
   * Split all the preprocessed data into training (70% of data) and testing (30% of data) sets. Each set consisted of train and test parts.
* ### Time To Apply Neutral Network:
   * Choose appropriate architecture for NN:
      * Number of layers
      * Numbers of neutrons
      * Activision function for each layer
   * Choose parameters for the model:
      * Optimerzer
      * Learning rate
      * Loss function
      * Metric
      * Number of epochs

