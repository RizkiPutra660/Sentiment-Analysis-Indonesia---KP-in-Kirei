# Sentiment-Analysis-Indonesia---KP-in-Kirei
Analyzing Indonesia tweets, is it positive, negative, or neutral.

## How to use
Scraping tweets has a purpose to train the machine learning model for labeling.
Usage steps:
1. Using GetOldTweets3. (see [GetOldTweets 3 Documentation](https://pypi.org/project/GetOldTweets3/) to install and scraping example).
2. Import your csv file to [Tweets_Cleaning_Indonesia.ipynb](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/blob/master/Tweets%20Cleaning%20Indonesia.ipynb) 
```python
DATASET_ENCODING = "ISO-8859-1"
data = pd.read_csv('Your_CSV_File.csv', encoding =DATASET_ENCODING, dtype={'text': "string"})
data['text']=data['text'].apply(str)
X = data.iloc[:,[2]]
```
3. Run the code. Wait until it finishes. 
4. After finished, you'll get a file named "Clean_Tweets_Indonesia.csv". Put this into [Prediction Using SVM.ipynb](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/blob/master/Training_data_dengan_Machine_Learning/Prediction%20Using%20SVM.ipynb).
5. Run until finished. In the end of the code, you'll see
  ```python
  review("")
  ```
Just type a sentence and you'll see the sentiment result (1 = positive, 0 = neutral, or -1 = negative).
6. The code will make a file named "classifier.sav" and "vectorizer.sav". Copy those files to [main_app](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/tree/master/Sentimen_Analisis_Indonesia_Web_App/main_app) folder. Those are Machine Learning model files.
7. Done! Now you can run the webapp.

## How to run the Webapp
1. Clone the repository.
2. open command prompt in [react-frontend](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/tree/master/Sentimen_Analisis_Indonesia_Web_App/react-frontend) folder, and type 
```bash
npm install
```
to install the front-end dependencies.
3. Inside the [Sentimen_Analisis_Indonesia_Web_App](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/tree/master/Sentimen_Analisis_Indonesia_Web_App)folder, type
```bash
python manage.py runserver
```
to run the application.
4. Enjoy!



