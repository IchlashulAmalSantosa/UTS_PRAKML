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

Model Naive Bayes diuji menggunakan 200 data uji dan menghasilkan evaluasi sebagai berikut:

**Akurasi: 0.775 (atau 77,5%)

              precision    recall  f1-score   support

           0       0.72      0.61      0.66        71
           1       0.80      0.87      0.83       129

    accuracy                           0.78       200
    macro avg      0.76      0.74      0.74       200
    weighted avg   0.77      0.78      0.77       200

Penjelasan:

-Model mencapai akurasi 77,5%, menunjukkan kinerja cukup baik.

-Kelas 1 (membeli komputer) memiliki kinerja lebih tinggi dibanding kelas 0.

-Precision dan recall lebih tinggi pada kelas mayoritas (1), yang umum dalam distribusi data tidak seimbang.

-Model dapat digunakan sebagai prediksi awal, meskipun bisa ditingkatkan lebih lanjut dengan teknik balancing atau model tambahan.
