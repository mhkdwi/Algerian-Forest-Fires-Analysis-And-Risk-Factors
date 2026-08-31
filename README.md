# Algerian Forest Fires Analysis & Risk Factors

Saya menganalisis data dari Kaggle yaitu data kejadian kebakaran hutan di dua wilayah di Aljazair (Algerian Forest Fires) pada tahun 2012. (https://www.kaggle.com/datasets/nitinchoudhary012/algerian-forest-fires-dataset)  

Aljazair merupakan negara terbesar di Afrika yang wilayah utaranya berbatasan langsung dengan Laut Mediterania. Negara ini memiliki iklim Mediterania dengan musim panas yang sangat kering dan panas, serta musim dingin yang cenderung basah dan hangat.  

Analisis ini berfokus pada 2 wilayah utama di utara Aljazair:  
1. Bejaia (Wilayah pesisir timur laut Aljazair)
2. Sidi Bel-Abbes (Wilayah pedalaman barat laut Aljazair)  

![Teks Alternatif](forest_fires.jpeg)
<p align="center"><i>Forest Fires</i></p>  

Data ini berisi pencatatan harian parameter cuaca (suhu, kelembapan, kecepatan angin, curah hujan) dan komponen Fire Weather Index (FWI) dari bulan Juni hingga September 2012, dengan total awal 244 baris data.  

Saya merapikan dan menyederhanakan data ini menggunakan Python dan Pandas untuk melakukan beberapa proses:  
1. Memisahkan stacked data (data bertumpuk) menjadi dua wilayah terpisah: Bejaia dan Sidi Bel-Abbes.  
2. Membersihkan whitespace liar pada nama kolom dan kategori label (fire / not fire).  
3. Mengubah tipe data numerik dan menghapus 1 baris dirty data yang tidak valid.  
4. Menambahkan kolom pendukung seperti nama bulan terurut (Jun, Jul, Aug, Sep).  

Data menjadi jauh lebih bersih (243 baris valid) dan siap untuk dianalisis secara akurat.  
(code bisa dilihat di file data_cleaning.py)  

Saya membuat sebuah dashboard di Power BI dari data yang telah dibersihkan  

![Teks Alternatif](dashboard.jpg)  

**Beberapa informasi dari dashboard:**  
1. Dari total 243 hari pengamatan, terjadi 137 kali insiden kebakaran hutan dengan tingkat risiko kejadian (fire rate) mencapai 56.4%. 
2. Rata-rata suhu udara saat terjadi kebakaran hutan adalah 33.8 °C.  
3. Sidi Bel-Abbes menjadi wilayah paling rawan kebakaran dengan total 79 insiden, jauh lebih tinggi dibandingkan Bejaia yang mencatatkan 58 insiden.  
4. Bulan Agustus merupakan puncak musim kebakaran hutan (peak month) dengan total 51 kejadian, seiring tingginya suhu udara dan musim kemarau kering di pertengahan tahun.  
5. Kebakaran hutan sangat masif terjadi pada rentang suhu > 30°C dan kelembapan udara (RH) < 60%. Saat suhu menembus di atas 35°C dengan kelembapan di bawah 40%, potensi terjadinya kebakaran hutan hampir mencapai 100%.  

**Strategi dan rekomendasi dari informasi yang ada:**  
1. Indikator suhu > 30°C dan kelembapan < 60% harus dijadikan Early Warning System (sistem peringatan dini). Ketika stasiun cuaca mencatat angka ini, status siaga bahaya kebakaran harus otomatis diaktifkan sebelum titik api pertama muncul.  
2. Membuat pos pemadam kebakaran utama, armada tangki air, dan pos pengawasan terutama di Sidi Bel-Abbes. Seperti menempatkan pemadam api di lokasi yang rumahnya paling mudah terbakar.  
3. Mulai akhir juli sampai agustus, mempersiapkan patroli ekstra 24 jam dan batasi aktivitas warga yang memicu percikan api di sekitar hutan seperti buang puntung rokok atau api unggun.
