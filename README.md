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
- **Preprocessing the reviews:** 
   * Used BeautifulSoup to parse the HTML content from the raw review data and collect the text content.
   * Tokenized the text content then:
      * Removed punctuation.
      * Removed stopwords.
      * Removed non-alphabetic words.
      * Used SnowBallStemmer, For example, the words 'walk', 'walked', 'walks' or 'walking' will be all converted to the base form 'walk'
   * Joined the list of preprocessed words<br/>
      ![Screenshot 2024-08-06 at 1 55 59 PM](https://github.com/user-attachments/assets/50e14e9b-c202-40b1-b86f-d1e4437be6b3)
- **Apply Feature Extraction Techniques:**
   * countVectorizer, to ignore words that appear too little or too much.
   * bag of words, will count how many of each word is in the sentence. Ex: 'the' appears 4 times in this sentence.
   * label encoder method to add numeric values for the labels, negative=0 and positive=1.
   * Split all the preprocessed data into training (70% of data) and testing (30% of data) sets. Each set consisted of train and test parts.<br/>
   ![Screenshot 2024-08-06 at 2 02 22 PM](https://github.com/user-attachments/assets/c5fc492b-e0e3-4cdc-ae35-5a62dc0f08b5)
- **Neutral Networks Time!**
   * Spilt the dataset into training and testing sets.
     ![Screenshot 2024-08-06 at 2 05 32 PM](https://github.com/user-attachments/assets/4cabfa2e-9a67-4a33-b5a4-eafd26118acd)
   * Configure the architecture for the Neutral Networks:
      * Number of layers
      * Numbers of neutrons
      * Activision function for each layer<br/>
        ![Screenshot 2024-08-06 at 2 07 51 PM](https://github.com/user-attachments/assets/7e62660e-27c7-409b-95e2-3401a9be8fae)
   * Choose more parameters:
      * Optimerzer
      * Learning rate
      * Loss function
      * Metric<br/>
        ![Screenshot 2024-08-06 at 2 10 10 PM](https://github.com/user-attachments/assets/d29050c3-8621-4b64-8f0f-87cbd24108ab)
   * Train/Test model:
      * set of epochs
        ![Screenshot 2024-08-06 at 2 10 57 PM](https://github.com/user-attachments/assets/f3a6f352-ece5-4e98-9050-977dedf8d9ab)
        
## Reflection 🤔
- If you have a model with a good training score like 96% but a testing score is 86%, this means your model is "overfitted". So, it is not always best to have the highest training score, you should also make sure that the testing score is not far behind.
- Neutral Networks is pretty awesome!


