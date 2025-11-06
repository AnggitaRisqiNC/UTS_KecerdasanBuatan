# Implementasi untuk Deteksi Ujaran Kebencian Otomatis Menggunakan Bidirectional LSTM pada Twitter

## Anggota Kelompok:

| No  | Nama                      | NIM       | Kelas        | Akun Github                                                          |
| --- | ------------------------- | --------- | ------------ | -------------------------------------------------------------------- |
| 1   | Anggita Risqi Nur Clarita | 312210450 | TI.22.A.SE.2 | [@AnggitaRisqiNC](https://github.com/AnggitaRisqiNC)                 |
| 2   | Faizah Via Fadhillah      | 312210460 | TI.22.A.SE.2 | [@FaizahviaFadhillah](https://github.com/FaizahviaFadhillah)         |
| 3   | Zahra Nurhaliza           | 312210364 | TI.22.A.SE.2 | [@ZahraNurhaliza](https://github.com/ZahraNurhaliza)                 |
| 4   | Muhammad Riyadus Solihin  | 312210404 | TI.22.A.SE.2 | [@muhammadriyadussolihin](https://github.com/muhammadriyadussolihin) |

### Paper Journal Kecerdasan Buatan
> **Journal:** [Implementasi untuk Deteksi Ujaran Kebencian Otomatis Menggunakan Bidirectional LSTM pada Twitter](https://github.com/AnggitaRisqiNC/UTS_KecerdasanBuatan/blob/7107fa1f9c228fa00a0f768f7ade66a19529a768/Journal%20Kecerdasan%20Buatan.docx)

## Ringkasan Mengenai Penelitian
Penelitian ini bertujuan untuk membangun model deteksi ujaran kebencian otomatis berbasis *Bidirectional Long Short-Term Memory* (Bi-LSTM) yang mampu mengidentifikasi teks berbahasa Indonesia pada media sosial Twitter. Proses penelitian mencakup tahapan *preprocessing* teks seperti *case folding*, penghapusan tanda baca, *stopword removal*, dan *lemmatization*, kemudian representasi data dilakukan menggunakan *embedding layer*. Model dilatih menggunakan fungsi *categorical cross-entropy* dan *optimizer* Adam dengan pembagian data pelatihan dan validasi yang seimbang. Hasil pengujian menunjukkan bahwa model Bi-LSTM yang dibangun memiliki tingkat akurasi sebesar 96,79%, *validation accuracy* sebesar 97%, dan *loss* sebesar 0,1675, yang menandakan kinerja sangat baik dalam mengklasifikasikan ujaran kebencian, non-kebencian, dan teks netral. Dengan demikian, metode Bi-LSTM terbukti efektif dalam mendeteksi ujaran kebencian otomatis pada teks berbahasa Indonesia.

### Mengapa Penelitian Ini Penting?
Dalam era digital saat ini, media sosial menjadi ruang utama bagi masyarakat untuk berinteraksi dan menyampaikan opini, namun juga menjadi wadah penyebaran ujaran kebencian yang dapat memicu konflik dan ketidaknyamanan di ruang publik. Permasalahan utama yang muncul adalah sulitnya mendeteksi ujaran kebencian secara manual karena jumlah data yang sangat besar dan sifat bahasa yang kompleks. Oleh karena itu, diperlukan sistem yang mampu mendeteksi dan mengklasifikasikan ujaran kebencian secara otomatis guna menjaga ruang digital tetap sehat dan kondusif.

### Dataset yang Digunakan
Dataset yang digunakan berasal dari dataset publik [Berita Bohong dan Ujaran Kebencian UU ITE](https://www.kaggle.com/datasets/pratamaazmi/berita-bohong-ujaran-kebencian-uu-ite-dataset) yang tersedia pada platform Kaggle. Dataset ini berisi teks komentar dan cuitan media sosial yang telah diberi label berdasarkan kandungan ujaran kebencian dengan tiga kategori:
  -  **0:** *Non-Hate Speech*: Teks tidak mengandung ujaran kebencian.
  -  **1:** *Hate Speech*/*Offensive Language*: Teks mengandung unsur kebencian atau hinaan.
  -  **2:** *Neutral*: Teks netral atau tidak dapat diklasifikasikan sebagai kebencian maupun non-kebencian.

### Preprocessing Teks
1. **Case Folding:** Semua teks diubah menjadi huruf kecil (lowercase).
2. **Penghapusan Tanda Baca dan Angka:** Tanda baca, simbol, dan angka dihilangkan.
3. **Tokenisasi:** Teks dipecah menjadi token (kata).
4. **Stopword Removal:** Kata-kata umum (stopwords) (misalnya, "yang", "dan") dihapus.
5. **Lemmatization:** Langkah ini mereduksi kata berimbuhan ke bentuk dasarnya (misalnya, "menghina" menjadi "hina").

### Metode, Algoritma dan Model
Metode yang Dipilih: **Embedding**. Metode ini menggunakan layers.Embedding dari TensorFlow/Keras, yang membuat representasi vektor padat untuk setiap kata dalam kosakata.

Penelitian ini menggunakan algoritma *Deep Learning*, khususnya *Bidirectional Long Short-Term Memory* (Bi-LSTM). Model dikembangkan menggunakan arsitektur jaringan saraf tiruan dengan lapisan Bi-LSTM, yang mampu membaca urutan kata dari kedua arah (*forward* dan *backward*) untuk memahami konteks linguistik yang lebih kompleks dan mendalam.

## Hasil dan Akurasi
Hasil evaluasi menunjukkan bahwa model *Bidirectional* LSTM mampu mencapai performa yang sangat baik dengan:
  -  **Akurasi:** `96,79%`
  -  **Validation Accuracy:** `97%`
  -  **Loss:** `0,1675`

Kinerja ini mengindikasikan bahwa model berhasil menangkap konteks semantik dan sintaksis bahasa Indonesia secara efektif dalam mengklasifikasikan ujaran kebencian, non-kebencian, dan teks netral.

## Finish
Kami ingin mengucapkan terima kasih yang sebesar-besarnya kepada semua pihak yang telah membantu kami dalam menyelesaikan project ini. Project ini merupakan hasil kerja keras dan dedikasi dari tim kami, dan kami sangat senang dapat membagikannya.

Kami ingin mengucapkan terima kasih juga kepada dosen pengampu mata kuliah Kecerdasan Buatan, **Pak Dr. Muhammad Fatchan, S.Kom., M.Kom.**, yang telah membantu kami dalam memahami konsep-konsep penting dalam Kecerdasan Buatan.
