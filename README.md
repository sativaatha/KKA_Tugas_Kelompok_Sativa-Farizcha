Laporan Analisis Data Penjualan dan Perilaku Pelanggan
Laporan ini disusun untuk memenuhi tugas praktikum analisis data menggunakan Python (Pandas, Matplotlib, Scikit-Learn).

1. Business Question
Dalam analisis ini, ada empat pertanyaan utama yang ingin dijawab:

Produk Underperformer: Kategori produk mana yang memiliki harga tinggi namun volume penjualannya rendah?

Segmentasi Pelanggan (RFM): Siapa saja pelanggan yang masuk kategori Champions dan Loyal yang berhak menerima voucher?

Efisiensi Iklan: Kategori produk mana yang memiliki rasio penjualan terhadap anggaran iklan (ROAS) paling rendah?

Dampak Iklan: Apakah anggaran iklan yang tinggi secara signifikan meningkatkan total penjualan?

2. Data Wrangling
Proses pembersihan dan manipulasi data yang dilakukan meliputi:

Konversi Tipe Data: Mengubah kolom Order_Date menjadi format datetime.

Handling Missing Values: Mengisi nilai kosong pada Total_Sales dengan hasil perkalian Quantity dan Price_Per_Unit.

Feature Engineering: * Membuat kolom Status (Normal vs Underperformer).

Menghitung skor RFM (Recency, Frequency, Monetary) untuk segmentasi pelanggan.

Menghitung kolom Efisiensi (Total Sales / Ad Budget).

3. Insights
Berdasarkan visualisasi yang telah dihasilkan:

A. Identifikasi Produk Underperformer
Insight: Produk kategori Home Decor teridentifikasi sebagai Underperformer. Meskipun harganya di atas rata-rata (Rp 1.029.583), kuantitas penjualannya paling rendah (71 unit).

B. Segmentasi Pelanggan (RFM)
Insight: Terdapat 25 pelanggan yang masuk kategori Champions dan Loyal. Kelompok Champions memiliki Recency yang sangat rendah (baru saja belanja) dan Monetary yang sangat tinggi (pengeluaran besar).

C. Efisiensi Anggaran Iklan
Insight: Kategori Gadget adalah yang paling tidak efisien dengan rasio 0.95x. Artinya, hasil penjualan lebih kecil daripada biaya iklan yang dikeluarkan (merugi secara operasional iklan).

D. Uji Hipotesis & Regresi
Insight: Hasil T-Test menunjukkan P-Value (0.7087) > 0.05, yang berarti tidak ada perbedaan signifikan antara iklan tinggi dan iklan rendah. Didukung oleh R2 Score (-0.07) pada model regresi, yang menunjukkan anggaran iklan saat ini bukan penentu utama total penjualan.

4. Recommendation
Berdasarkan hasil analisis, berikut saran untuk perusahaan:

Evaluasi Produk Home Decor: Lakukan promosi khusus atau tinjau kembali strategi harga untuk kategori ini agar volume penjualan meningkat.

Program Loyalitas: Segera distribusikan voucher loyalitas kepada 25 pelanggan terpilih (kategori Champions dan Loyal) untuk menjaga retensi.

Optimalisasi Iklan Gadget: Hentikan atau evaluasi ulang strategi kreatif pada iklan kategori Gadget karena saat ini memberikan hasil di bawah biaya pengeluaran (Break-even < 1x).

Eksplorasi Faktor Lain: Karena iklan tidak berpengaruh signifikan, perusahaan perlu meneliti faktor lain yang mendorong penjualan, seperti kualitas produk, ulasan pelanggan, atau tren musiman.
