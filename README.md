# Sentiment-Analysis-Indonesia---KP-di-Kirei
Menganalisis tweets bahasa indonesia, apakah itu positif, negatif, atau netral.

## Cara Penggunaan
Scraping tweets bertujuan untuk melatih model machine learning untuk dilakukan pelabelan.
Langkah-langkah Penggunaan:
1. menggunakan fungsi GetOldTweets3. (lihat [GetOldTweets 3 Documentation](https://pypi.org/project/GetOldTweets3/) untuk menginstal dan mengambil tweets).
2. Impor csv anda ke file [Tweets_Cleaning_Indonesia.ipynb](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/blob/master/Tweets%20Cleaning%20Indonesia.ipynb) 
```python
DATASET_ENCODING = "ISO-8859-1"
data = pd.read_csv('Your_CSV_File.csv', encoding =DATASET_ENCODING, dtype={'text': "string"})
data['text']=data['text'].apply(str)
X = data.iloc[:,[2]]
```
3. Jalankan kodenya dan tunggu sampai selesai. 
4. Setelah selesai, anda akan mendapatkan file bernama "Clean_Tweets_Indonesia.csv". Masukan file ini ke [Prediction Using SVM.ipynb](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/blob/master/Training_data_dengan_Machine_Learning/Prediction%20Using%20SVM.ipynb).
5. Jalankan hingga selesai. pada akhir kode, anda akan melihat
  ```python
  review("")
  ```
Cukup ketik kalimat dan anda akan melihat hasil sentimen (1 = positif, 0 = netral, atau -1 = negatif).

6. Kode tersebut akan membuat file bernama "classifier.sav" dan "vectorizer.sav". Salin file-file tersebut ke [main_app](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/tree/master/Sentimen_Analisis_Indonesia_Web_App/main_app) folder. Itu adalah file model Machine Learning.

7. Selesai! Sekarang Anda dapat menjalankan aplikasi web.

## How to run the Webapp
1. Kloning repositori.
2. buka command prompt di [react-frontend](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/tree/master/Sentimen_Analisis_Indonesia_Web_App/react-frontend) folder, dan ketik 
```bash
npm install
```
untuk menginstal dependensi front-end.

3. Di dalam [Sentimen_Analisis_Indonesia_Web_App](https://github.com/RizkiPutra660/Sentiment-Analysis-Indonesia---KP-in-Kirei/tree/master/Sentimen_Analisis_Indonesia_Web_App) folder, ketikan
```bash
python manage.py runserver
```
untuk menjalankan aplikasi.

4. Enjoy!
