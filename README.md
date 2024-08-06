# IMDB Sentiment Analysis

![Screenshot 2024-08-06 at 1 45 37 PM](https://github.com/user-attachments/assets/a5619649-f130-4bba-86dd-6df84f5c5709)

## Objective 📋
Attempt to build a reliable deep-learning model using Neutral Networks algorithm to predict the correct sentiment for IMBD movie reviews with a dataset of 50000 rows.

## Tech Stack 🧰
- Python
- Pandas
- TensorFlow
- Scikit-learn
- Deep Learning and Neural Networks

[Dataset source](https://ai.stanford.edu/~amaas/data/sentiment/)

## Steps taken 🪜
- **Collecting Data:**
    * Reads the IMDB movie reviews data stored in the CSV file into a pandas DataFrame.
      
    * Selected 8000 reviews since the dataset was quite large and consisted of 25,000 reviews.
    * Checked if the dataset labels were balanced.
    * Separated main Dataframe into two: reviews (features) and sentiment (labels).
- **PreProcessing The Data For ML:** 
   * Used BeautifulSoup to parse the HTML content from the raw review data and collect the text content.
   * Tokenized the text content then:
      * Removed punctuation
      * Removed stopwords
      * Removed non-alphabetic words
      * Used SnowBallStemmer to stem each word
   * Joined the list of preprocessed words
- **Prepare Data For Neutral Network:**  
   * Used the bag of words method to extract the features from the preprocessed movie reviews.
   * Used the label encoder method to add numeric values for the string labels (0=negative, 1=positive).
   * Split all the preprocessed data into training (70% of data) and testing (30% of data) sets. Each set consisted of train and test parts.

- **Time To Apply Neutral Network:**
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

