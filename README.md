# IMDB Sentiment Analysis

![Screenshot 2024-08-06 at 1 45 37 PM](https://github.com/user-attachments/assets/a5619649-f130-4bba-86dd-6df84f5c5709)

## Objective 📋
Attempt to build a reliable deep-learning model using Neutral Networks algorithm to predict the correct sentiment for IMBD movie reviews with a dataset of 50000 rows.

## Tech Stack 🧰
- TensorFlow (Deep Learning - Neutral Networks)
- Scikit-learn
- Python (
- Pandas
- Matplotlib
- Seaborn
- BeautifulSoup
- [Dataset source](https://ai.stanford.edu/~amaas/data/sentiment/)

## Steps taken 🪜
- **Collecting Data:**
    * Reads the dataset of 50,000 IMDB movie reviews stored in the CSV file into a pandas Dataframe.<br/>
      ![Screenshot 2024-08-06 at 1 52 02 PM](https://github.com/user-attachments/assets/da1fadb5-96c3-4359-996e-f185bce69b01)
    * Checked if the dataset labels were balanced.<br/>
      ![Screenshot 2024-08-06 at 1 52 11 PM](https://github.com/user-attachments/assets/46c74891-0370-4336-b09d-8dc5ac5c587a)
    * Separated main Dataframe into two: reviews (features) and sentiment (labels).<br/>
      ![Screenshot 2024-08-06 at 1 54 00 PM](https://github.com/user-attachments/assets/cd4c122f-a6b5-4458-9518-6f44a2375b95)


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

