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

Model Naive Bayes berhasil melakukan klasifikasi dengan performa sebagai berikut:

