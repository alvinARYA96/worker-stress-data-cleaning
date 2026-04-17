#  Data Cleaning: Worker Stress Survey Dataset
## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk mendemonstrasikan proses *end-to-end data cleaning* pada dataset survei pekerja. Fokus utama adalah mengubah data mentah yang memiliki banyak anomali menjadi dataset yang siap digunakan untuk analisis statistik

Proyek ini merupakan bagian dari tugas **DigitalSkola Data Analyst Bootcamp**.

## 📊 Dataset Overview
Dataset berisi **7.917 baris** responden dengan **10 kolom** informasi, termasuk:
- **Demografis:** Umur, Jenis Kelamin, Pendidikan, Status Pernikahan.
- **Kondisi Kerja:** Pekerjaan, Gaji.
- **Kesehatan & Kebiasaan:** Berat Badan, Tinggi Badan, Status Merokok, Pernah Stress.

## 🛠️ Alur Pembersihan Data
Proses pembersihan dilakukan dengan tahapan sebagai berikut:

1.  **Data Profiling:** Memeriksa dimensi data, tipe data, dan deteksi dini nilai kosong.
2.  **Handling Duplicates:** Menghapus 82 baris data identik untuk menghindari bias perhitungan.
3.  **Handling Missing Values:**
    * **Drop Row:** Dilakukan pada kolom numerik (`umur`, `gaji`, dll) karena persentase kehilangan < 2%.
    * **Imputasi Modus:** Dilakukan pada kolom kategorikal dan biner.
4.  **Outlier Management:**
    * Menghapus data tidak masuk akal (contoh: umur negatif).
    * Mempertahankan data ekstrem yang valid berdasarkan logika bisnis (contoh: gaji profesional yang tinggi).
5.  **Data Inconsistency:** Standardisasi format teks (*Title Case*) dan perbaikan tipe data (mengubah *float* menjadi *integer*).
