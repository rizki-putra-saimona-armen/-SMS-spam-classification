#  SMS Spam Classification using NLP & Naive Bayes

Repository ini berisi proyek *Machine Learning* untuk klasifikasi teks (*Text Classification*) yang bertujuan untuk mendeteksi apakah sebuah pesan SMS tergolong sebagai **Spam** (pesan massal/penipuan/iklan) atau **Ham** (pesan normal/pribadi). Proyek ini menerapkan konsep dasar **Natural Language Processing (NLP)** untuk ekstraksi fitur teks.

##  Fitur Utama Proyek
* **Text Preprocessing & Tokenization:** Mengubah korpus data teks mentah menjadi representasi numerik yang siap diproses oleh algoritma komputer.
* **TF-IDF Vectorizer:** Implementasi `TfidfVectorizer` untuk menghitung bobot kepentingan suatu kata berdasarkan kemunculannya di dalam satu pesan relatif terhadap seluruh dokumen (SMS) di dalam dataset.
* **Multinomial Naive Bayes:** Penggunaan algoritma `MultinomialNB` yang sangat efisien, cepat, dan menjadi standar industri untuk pemrosesan klasifikasi data teks/hitungan distribusi frekuensi kata.
* **Robust Text Pipeline:** Penggabungan proses ekstraksi TF-IDF dan model Naive Bayes ke dalam satu arsitektur `Pipeline` Scikit-Learn guna mencegah terjadinya *Data Leakage*.
* **Model Validation & Deployment Ready:** Proses optimasi parameter menggunakan `RandomizedSearchCV` dan penyimpanan otomatis model terbaik ke dalam format berkas *pickle*.

---

##  Bagaimana TF-IDF & Naive Bayes Bekerja?

1. **TF-IDF (Term Frequency - Inverse Document Frequency):**
   Metode ini memberikan bobot tinggi pada kata-kata yang unik dan mencirikan suatu pesan (misal kata: *"PROMO"*, *"MENANG"*, *"HADIAH"* pada SMS spam), dan memberikan bobot rendah pada kata umum yang sering muncul di semua SMS (seperti: *"yang"*, *"di"*, *"dan"*).
2. **Multinomial Naive Bayes:**
   Berdasarkan teorema probabilitas Bayes, algoritma ini menghitung peluang suatu SMS masuk ke kategori *Spam* atau *Ham* berdasarkan kombinasi kata-kata yang ada di dalam SMS tersebut. Algoritma ini bekerja sangat cepat walaupun menangani ribuan dimensi kata unik (*vocabulary*).

---

##  Tech Stack & Library
* **Python** (Bahasa Pemrograman Utama)
* **Jupyter Notebook** (`.ipynb`)
* **Pandas & NumPy** (Analisis Struktur Data & Array)
* **Scikit-Learn** (`MultinomialNB`, `TfidfVectorizer`, `Pipeline`, `RandomizedSearchCV`)
* **jcopml** (Ekstensi *helper pipeline*, tuning parameter teks, dan *automated saving model*)

---

##  Cara Menjalankan Proyek

1. **Clone Repositori Ini:**
   ```bash
   git clone [https://github.com/username-kamu/nama-repositori.git](https://github.com/username-kamu/nama-repositori.git)
   cd nama-repositori
