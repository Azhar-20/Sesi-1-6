# Dokumentasi Studi Kasus Seminar Informatika (Sesi 1 - 6)

Repositori ini memuat implementasi studi kasus berbasis kode Python untuk setiap sesi materi seminar, mulai dari analitik bisnis, komputasi paralel, geospasial, machine learning, desain interaksi antarmuka, hingga analisis penginderaan jauh berbasis satelit.

---

### Sesi 1: Make Sense of Data with Analysis and AI
* **Narasumber**: Andria Arisal, S.T., M.Eng. (Pusat Riset Sains Data dan Informasi - BRIN)
* **Topik Kasus**: Mitigasi Piutang Macet Menggunakan Framework CRISP-DM dan 4 Tingkat Analitik
* **Penjelasan & Implementasi**:
  * **Data Preparation**: Menerapkan pembersihan data mentah dan imputasi nilai kosong guna menghindari prinsip *garbage in, garbage out*.
  * **4 Tingkat Analisis**:
    1. *Deskriptif*: Menghitung ringkasan volume piutang dan persentase faktur berisiko gagal bayar.
    2. *Diagnostik*: Mengidentifikasi pola hubungan antara tingginya diskon penjualan dengan keterlambatan pembayaran piutang.
    3. *Prediktif*: Melatih model *Logistic Regression* untuk memprediksi probabilitas gagal bayar pada faktur baru.
    4. *Preskriptif*: Menghasilkan rekomendasi tindakan bisnis otomatis (penolakan kredit, pembatasan tenor, atau persetujuan standar) berdasarkan estimasi probabilitas risiko.

---

### Sesi 2: Bridging Global Infrastructure to Address Local Challenges with HPC
* **Narasumber**: Asst. Prof. Dr. Worawan Diaz Carbalo (Thammasat University, Thailand)
* **Topik Kasus**: Simulasi Prediksi Difusi Polusi PM2.5 Skala Lokal Menggunakan Komputasi Paralel Multi-Core
* **Penjelasan & Implementasi**:
  * **HPC untuk Solusi Lokal**: Memodelkan dinamika difusi polusi udara berbasis grid numerik 2D berukuran besar untuk memangkas waktu prakiraan kualitas udara lokal.
  * **Akselerasi Paralel**: Memanfaatkan modul `multiprocessing` pada Python untuk membagi beban komputasi matriks ke seluruh inti CPU (*multi-core*), serta membandingkan performa komputasi sekuensial tunggal dengan pemrosesan paralel guna mengukur faktor percepatan (*speedup*).

---

### Sesi 3: Career and Competition in Industrial Era with GIS
* **Narasumber**: Widi Primadepa, S.Kom. (Asset Management GIS Analyst di City Care Property, Selandia Baru)
* **Topik Kasus**: Otomatisasi Penilaian Kondisi Aset Infrastruktur dan Analisis Spasial
* **Penjelasan & Implementasi**:
  * **Peran Pengembang (Developer GIS)**: Membangun pipeline analisis otomatis tanpa ketergantungan perangkat lunak berbayar (*proprietary*).
  * **Analisis Geospasial**: Menghitung jarak lengkung bumi (*Haversine Formula*) antara aset infrastruktur dan episentrum zona rawan bencana (*hazard buffer zone*).
  * **Standar Industri**: Menghitung skor kesehatan aset secara otomatis dan mengekspor hasilnya ke format standar terbuka *GeoJSON FeatureCollection*.

---

### Sesi 4: Introduction to Machine Learning
* **Narasumber**: Dr. Taniza binti Tajuddin (Universiti Teknologi MARA / UiTM, Malaysia)
* **Topik Kasus**: Klasifikasi Persetujuan Pinjaman Menggunakan Alur Kerja Machine Learning
* **Penjelasan & Implementasi**:
  * **ML Workflow Terstruktur**: Menjalankan tahapan pengumpulan data, standarisasi fitur numerik (*StandardScaler*), serta pembagian data (*data splitting*) 80% data latih dan 20% data uji.
  * **Supervised Learning**: Menggunakan algoritma *Random Forest Classifier* untuk mencegah risiko *overfitting*.
  * **Evaluasi Komprehensif**: Menguji keandalan model menggunakan *Confusion Matrix*, *Precision*, *Recall*, dan *F1-Score* untuk memastikan keputusan prediksi yang seimbang dan adil.

---

### Sesi 5: Human-Computer Interaction & Data Visualization
* **Narasumber**: Dr. Arafat Febriandirza (Kepala Kelompok Riset IMK & Visualisasi - BRIN)
* **Topik Kasus**: Perancangan Dasbor Analitik Interaktif Berbasis Psikologi Kognitif & Prinsip IMK
* **Penjelasan & Implementasi**:
  * **Beban Kognitif & Batas Memori Kerja**: Menyusun ringkasan informasi metrik sistem ke dalam kapasitas memori kerja manusia ($7 \pm 2$ chunks) untuk meminimalkan beban kognitif berlebih (*extraneous cognitive load*).
  * **Fitur Visual Preatentif & Gestalt**: Menggunakan kartu (*card layout/enclosure*) serta warna status preatentif kontras (hijau, kuning, merah) agar indikator kritis langsung dikenali pengguna secara spontan.
  * **Prinsip Interaksi**: Menerapkan konsep *Visibility*, *Affordance*, dan penyediaan umpan balik instan (*system feedback*) saat pengguna berinteraksi dengan elemen antarmuka.

---

### Sesi 6: Attributing Direct Drivers to Deforestation Alerts with Satellite Imagery and AI
* **Narasumber**: Dr. Bart Slagter (Laboratory of Geo-Information Science & Remote Sensing)
* **Topik Kasus**: Klasifikasi Penyebab Langsung (*Direct Drivers*) Peringatan Deforestasi Citra Satelit
* **Penjelasan & Implementasi**:
  * **Integrasi AI & Penginderaan Jauh**: Menghubungkan peringatan titik hilangnya tutupan kanopi dengan indeks spektral satelit (penurunan vegetasi NDVI dan indeks kebakaran NBR) serta parameter spasial (jarak ke jalan eksisting dan luas area bukaan).
  * **Atribusi Driver**: Melatih model klasifikasi untuk menentukan penyebab langsung secara otomatis, membedakan antara kejadian Kebakaran Hutan dan Lahan (Karhutla), Perkebunan Sawit, Pembangunan Jalan, dan Perambahan Skala Kecil.
