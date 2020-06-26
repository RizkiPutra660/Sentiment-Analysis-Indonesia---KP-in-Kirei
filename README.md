# Sentiment-Analysis-Indonesia---KP-in-Kirei
Analyzing Indonesia tweets, is it positive, negative, or neutral.

## How to scrape tweets
Scraping tweets has a purpose to train the machine learning model for labeling.
Usage steps:
1. Using GetOldTweets3. (see [GetOldTweets 3 Documentation](https://pypi.org/project/GetOldTweets3/) to install and scraping example).
2. Import your csv file to [Tweets Cleaning Indonesia.ipynb](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/blob/master/Tweets%20Cleaning%20Indonesia.ipynb) 
```python
DATASET_ENCODING = "ISO-8859-1"
data = pd.read_csv('Your_CSV_File.csv', encoding =DATASET_ENCODING, dtype={'text': "string"})
data['text']=data['text'].apply(str)
X = data.iloc[:,[2]]
```
3. Run the code. Wait until it finishes. 
4. After finished, you'll get a file named "Clean_Tweets_Indonesia.csv". Put this into [Sentiment Analysis Indonesia.ipynb](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/blob/master/Sentiment%20Analysis%20Indonesia.ipynb).
5. Run until finished. In the end of the code, you'll see
  ```python
  predict("")
  ```
  Just type a sentence and you'll see the sentiment result (positive, neutral, or negative) with score
