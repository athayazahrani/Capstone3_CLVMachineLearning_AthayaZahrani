# Customer Lifetime Value (CLV) Prediction using Machine Learning Algorithm
## Athaya Zahrani Irmansyah as a Purwadhika JCDS-0408 Student On Site Bandung 2024 / Capstone Project Module 3 Machine Learning (in Bahasa)

## Context
   Bagi perusahaan, memperoleh pelanggan baru memerlukan usaha lebih sulit dibandingkan mempertahankan pelanggan yang sudah ada. Oleh karena itu, mempertahankan pelanggan (*customer retention*) menjadi kunci untuk menjaga pendapatan yang stabil bagi perusahaan, karena pembelian berulang dari pelanggan yang sudah ada memungkinkan bisnis tetap berjalan. Oleh karena itu, perusahaan perlu mengukur seberapa bernilai pelanggan bagi bisnis mereka. Salah satu metrik yang dapat digunakan untuk mengukur hal ini adalah `Customer Lifetime Value (CLV)`.

CLV adalah metrik yang sangat penting dalam manajemen bisnis modern. Dengan membantu perusahaan memahami nilai jangka panjang dari pelanggan mereka, CLV memungkinkan perusahaan untuk membuat keputusan yang lebih cerdas dan strategis dalam hal pemasaran, retensi, dan pengembangan produk. Meningkatkan CLV secara langsung berkaitan dengan peningkatan profitabilitas dan stabilitas bisnis, menjadikannya alat yang sangat berharga dalam pengelolaan hubungan pelanggan.

CLV adalah jumlah total uang yang dihabiskan oleh pelanggan untuk perusahaan selama hubungan bisnis antara pelanggan dan perusahaan tersebut berjalan. Secara sederhana, `CLV adalah perkiraan nilai total pendapatan yang dapat dihasilkan dari pelanggan`. Dalam praktiknya, metrik CLV sering digunakan oleh perusahaan yang mengandalkan penjualan berulang (seperti perusahaan makanan atau produk rumah tangga) dan perusahaan dengan model bisnis berlangganan (seperti asuransi dan perusahaan telekomunikasi).

## Problem Statement
Dataset yang digunakan pada analisis ini adalah `'data_customer_lifetime_value.csv'`. Berdasarkan data tersebut, dapat ditarik kesimpulan untuk suatu *problem statement*, yaitu mengenai `perusahaan asuransi mobil yang sedang menghadapi masalah dalam meningkatkan pendapatannya`. Salah satu kemungkinan penyebab utamanya adalah pendekatan strategi pemasaran yang kurang tepat, di mana perusahaan mengalokasikan anggaran yang sama untuk semua jenis pelanggan. Akibatnya, perusahaan menghabiskan lebih banyak uang untuk pelanggan dengan nilai rendah (*low-value customer*) dan kehilangan pelanggan dengan nilai tinggi (*high-value customer*). Untuk mengatasi masalah ini, perusahaan meminta tim *data scientist* untuk menggunakan metrik CLV demi menentukan seberapa bernilai setiap pelanggan dan menyesuaikan strategi pemasaran berdasarkan nilai tersebut. Namun, saat ini perusahaan belum memiliki sistem yang dapat memprediksi CLV dengan cepat dan akurat, sehingga penentuan strategi pemasaran menjadi lebih lambat karena masih dilakukan secara manual. Oleh karena itu, `prediksi CLV yang lebih cepat dan akurat (menggunakan algoritma *machine learning*) sangat penting untuk mendukung pengambilan keputusan pemasaran yang lebih tepat dan efektif`.

## Goals
Berdasarkan penjelasan *problem statement* di poin 2, akan sangat membantu bagi perusahaan asuransi mobil (khususnya divisi pemasaran) jika tersedia sebuah alat yang dapat memprediksi CLV dengan memanfaatkan data demografis dan data asuransi mobil pelanggan seperti yang tertera pada nama kolom dataset (`'Vehicle Class', 'Coverage', 'Renew Offer Type', 'EmploymentStatus', 'Marital Status', 'Education', 'Number of Policies', 'Monthly Premium Auto', 'Total Claim Amount', 'Income', dan 'Customer Lifetime Value'`). Dengan adanya algoritma *machine learning* sebagai alat bantu ini, diharapkan pengolahan data CLV tidak lagi harus dilakukan secara manual, sehingga dapat mempercepat proses pengambilan keputusan dalam strategi pemasaran, demi mencapai pentingnya CSV, antara lain:

1. **Optimasi Pengeluaran Pemasaran:** Dengan memahami CLV, perusahaan dapat menentukan berapa banyak yang seharusnya mereka keluarkan untuk mendapatkan pelanggan baru tanpa mengorbankan profitabilitas. CLV membantu dalam mengidentifikasi apakah kampanye pemasaran efisien dan apakah mereka berhasil menarik pelanggan yang bernilai tinggi.

2. **Strategi Retensi Pelanggan:** CLV memberikan wawasan tentang pentingnya mempertahankan pelanggan yang ada. Dengan fokus pada peningkatan retensi pelanggan, perusahaan dapat meningkatkan CLV mereka dan, oleh karena itu, meningkatkan total pendapatan. Pelanggan yang tetap setia lebih cenderung melakukan pembelian berulang, memberikan rekomendasi, dan bertahan lebih lama dengan perusahaan.

3. **Segmentasi Pelanggan:** Perusahaan dapat menggunakan CLV untuk mengelompokkan pelanggan berdasarkan nilai mereka. Ini memungkinkan perusahaan untuk memberikan perhatian khusus pada segmen pelanggan yang paling menguntungkan dan merancang penawaran khusus untuk mempertahankan dan meningkatkan nilai mereka.

4. **Perencanaan Anggaran dan Sumber Daya:** Memahami CLV membantu perusahaan dalam merencanakan anggaran dan mengalokasikan sumber daya lebih efisien. Dengan fokus pada pelanggan dengan CLV tinggi, perusahaan dapat memprioritaskan inisiatif yang memberikan pengembalian investasi terbaik.

5. **Pengembangan Produk dan Layanan:** CLV juga dapat memandu pengembangan produk dan layanan baru. Dengan mengetahui apa yang membuat pelanggan berharga tetap setia, perusahaan dapat menyesuaikan produk dan layanan mereka untuk memenuhi kebutuhan pelanggan tersebut, meningkatkan kepuasan, dan memperpanjang durasi hubungan pelanggan.

## Analytic Approach
   Langkah yang akan dilakukan adalah menganalisis data yang diperoleh untuk mengidentifikasi pola dari berbagai fitur yang ada, yang dapat membedakan CLV pada masing-masing pelanggan. Model regresi akan digunakan untuk membantu perusahaan dalam menyediakan alat prediksi CLV dengan bantuan algoritma *machine learning*. Secara detail, analisis yang akan dilakukan adalah sebagai berikut:
- Melakukan *Explantory Data Analysis (EDA)* pada dataset. 
- Melakukan *Preprocessing* pada dataset.
- Melakukan *Benchmarking* pada beberapa model regresi untuk memilih model yang paling tepat untuk dataset.
- Melakukan *Hyperparameter* Tuning pada model terpilih untuk mendapatkan hasil *error* yang lebih rendah.

## Metric Evaluation
  Metrik evaluasi yang akan digunakan adalah `RMSE, MAE, dan MAPE` dengan keterangan sebagai berikut:
1. `RMSE`: Root Mean Square Error (Rataan Akar Kuadrat dari Error)
2. `MAE`: Mean Absolute Error (Rataan Nilai Absolut dari Error)
3. `MAPE`: Mean Absolute Percentage Error (Rataan Persentase Absolut dari Error)

Dari perhitungan yang nanti diperoleh, kita akan mengecek bahwa jika `semakin kecil nilai RMSE, MAE, dan MAPE yang dihasilkan, maka semakin akurat model tersebut dalam memprediksi CLV sesuai dengan batasan fitur yang digunakan`. Perumusan perhitungan RMSE, MAE, dan MAPE disajikan pada gambar di bawah. Pembahasan lebih lanjut akan dijelaskan dengan detail di tahapan selanjutnya.
