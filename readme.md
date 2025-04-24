#  Klasifikasi Keputusan Pembelian Komputer dengan Naive Bayes

##  Deskripsi Dataset

Dataset ini berisi informasi demografis dan kebiasaan pengguna yang digunakan untuk memprediksi apakah seseorang akan membeli komputer atau tidak. Dataset terdiri dari beberapa fitur kategorikal:

- `Age`: Umur pengguna (Tua, Paruh Baya, Muda)
- `Income`: Pendapatan pengguna (Tinggi, Sedang, Rendah)
- `Student`: Apakah pengguna adalah mahasiswa (Ya atau Tidak)
- `Credit_Rating`: Status kredit pengguna (Baik atau Buruk)
- `Buys_Computer`: Label target, 1 untuk membeli komputer, 0 untuk tidak membeli

Dataset ini merupakan contoh klasik untuk klasifikasi dengan data kategorikal.

---

##  Tujuan Klasifikasi

Tujuan dari proyek ini adalah membangun model klasifikasi menggunakan algoritma **Naive Bayes** untuk memprediksi keputusan seseorang dalam membeli komputer berdasarkan data demografis dan status keuangan.

---

##  Algoritma: Naive Bayes

Karena NIM saya berakhiran **genap**, maka algoritma yang digunakan adalah **Naive Bayes**. Pendekatan yang digunakan adalah **Gaussian Naive Bayes**, dengan sebelumnya melakukan **One-Hot Encoding** terhadap fitur kategorikal.

---

##  Tahapan Preprocessing

1. **Membaca dataset** dari file CSV.
2. **Melakukan One-Hot Encoding** terhadap fitur-fitur kategorikal (`Age`, `Income`, `Student`, `Credit_Rating`).
3. **Memisahkan fitur dan label** (`Buys_Computer`).
4. **Split data** menjadi data latih dan uji (80% : 20%).
5. **Melatih model** menggunakan `GaussianNB`.
6. **Mengevaluasi model** dengan metrik akurasi, precision, recall, f1-score, dan confusion matrix.
7. **Menyimpan hasil evaluasi** ke dalam folder `results`.

---

##  Hasil Evaluasi

Model Naive Bayes diuji menggunakan data uji sebanyak 10 data (20% dari total data), dan memberikan hasil evaluasi sebagai berikut:

              precision    recall  f1-score   support

           0       0.75      0.75      0.75         4
           1       0.83      0.83      0.83         6

    accuracy                           0.80        10
    macro avg      0.79      0.79      0.79        10
    weighted avg   0.80      0.80      0.80        10

Penjelasan:

-Akurasi: 80% — artinya 8 dari 10 prediksi model benar.

-Precision 0 (tidak membeli): 75% — dari semua yang diprediksi tidak membeli, 75% benar.

-Recall 0: 75% — dari semua yang benar-benar tidak membeli, 75% berhasil dikenali.

-Precision 1 (membeli): 83%

-Recall 1: 83%

-F1-score: Seimbang antara precision dan recall untuk kedua kelas.

Model cukup seimbang dan mampu membedakan antara kelas pembeli dan bukan pembeli dengan performa yang memuaskan, terutama untuk dataset kecil seperti ini.

