# FootballManager21---Striker-Classification
Latihan melakukan supervised machine learning dengan menggunakan data pemain sepak bola dari game Football Manager 21

## Pendahuluan


## Data
Data yang digunakan dalam analisis ini menggunakan data yang diambil langsung dari game melalui fitur in-game print screen yang dicetak ke dalam format html yang kemudian di konversi menjadi file csv. Cara ini memungkinkan untuk melakukan filter data dari game terlebih dahulu sebelum di ekspor ke dataset. Data yang diambil untuk analisis ini adalah pemain sepak bola dengan kemamapuan saat ini atau dengan kemampuan potensial untuk bermain di kompetisi kasta tertinggi. Versi database game yang digunakan adalah:
  * Football Manager 21 Official Database version 21.4.0
  * FMI Update 21.12 - DEADLINE UPDATE

## Metode Analisis
Terdapat tiga metode machine learning yang digunakan dalam analisa ini yaitu:
  * Logistic regression (logit)
  * K Nearest Neighbors (K-NN)
  * Random forest

Dalam melakukan analisis, analisis dilakukan dengan menggunakan fitur yang berbeda yaitu:
  * Analisis menggunakan seluruh fitur
  * Analisis menggunakan fitur yang secara teori menjelaskan kemampuan yang seharusnya dimiliki oleh seorang penyerang

Karena data yang dimiliki bersifat imbalance, maka dalam analisis juga dilakukan dengan dua jenis data yang berbeda yaitu:
  * Data imbalance (data original)
  * Data Balanced, data original yang ditreatment dengan melakukan oversampling dengan teknik SMOTE

Sehingga secara total terdapat 12 model yang akan dijalankan pada analisis ini. Kemudian ke 12 model tersebut akan dievaluasi dengan membandingkan nilai F1 score dari setiap model untuk menentukan model terbaik. Nilai F1 score dipilih sebagai metrik evaluasi karena analisis ini berusaha untuk meminimalkan nilai observasi yang false positif dan false negatif dalam model.

## Hasil
Dari hasil evaluasi metrik 12 model yang dijalankan, model terbaik untuk data ini adalah **model random forest yang menggunakan seluruh fitur dengan data balanced**. Model tersebut memiliki nilai F1 score sebesar 0.9729 dengan nilai presisi 0.9623 dan nilai recall 0.9838
