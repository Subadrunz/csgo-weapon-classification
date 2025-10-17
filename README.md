# Tugas 4 Machine Learning: Ekstraksi Fitur Gambar

## 📋 Deskripsi

Program untuk mengekstrak fitur dari dataset gambar senjata CSGO menggunakan berbagai teknik computer vision. Program ini menghasilkan file features yang siap digunakan untuk machine learning.

**Dibuat oleh:** [Rizki Jailani]  
**Kelas:** [05TPLP004]  
**NIM:** [231011401758]  
**Tanggal:** Oktober 2025

## 🎯 Fitur yang Diekstrak

- 🎨 **Fitur Warna** (159 fitur): Histogram RGB, HSV, statistik warna
- 🔍 **Fitur Tekstur** (102 fitur): LBP, GLCM
- 📐 **Fitur Bentuk** (35 fitur): Canny edges, Hu moments, contour features
- 📍 **Fitur Lokal** (96 fitur): ORB descriptors
- 🏗️ **Fitur Struktural** (1,764 fitur): HOG (Histogram of Oriented Gradients)

**Total: 2,156 fitur per gambar**

## 📊 Dataset

- **Sumber:** CSGO Guns Dataset
- **Jumlah:** 893 gambar
- **Format File:** `weapon_namasenjata_deskripsi.jpg`
- **Contoh:** `weapon_ak47_sp_spray_jungle_light_large.jpg`
- **Kelas:** ak47, m4a1, awp, deagle, fiveseven, dll

## 🚀 Cara Menjalankan Program

### 1. Install Dependencies

```bash
pip install -r requirements.txt

2. Siapkan Dataset
Buat folder dataset/
Masukkan semua gambar ke folder tersebut
Format nama: weapon_namasenjata_....jpg

3. Jalankan Program
Buka ekstrak_fitur.ipynb di Jupyter Notebook dan run semua cell secara berurutan.

4. Tunggu Hingga Selesai
Progress akan ditampilkan di progress bar
Estimasi waktu: 30-60 menit untuk 893 gambar
Output akan tersimpan di folder output_features/

📁 Struktur Project
Tugas_Extraction_Fitur_[KodeKelas]/
├── 📓 ekstrak_fitur.ipynb          # Program utama
├── 📁 dataset/                          # Folder gambar
│   ├── weapon_ak47_...jpg
│   ├── weapon_m4a1_...jpg
│   └── ...
├── 📁 output_features/                  # HASIL EKSTRAKSI
│   ├── all_features.csv                 # Fitur mentah
│   ├── features_normalized.csv          # Fitur ternormalisasi
│   ├── features.npy                     # Format NumPy
│   ├── scaler.pkl                       # Scaler normalisasi
│   └── feature_names.txt                # Daftar nama fitur
├── 📄 requirements.txt                  # Daftar library
└── 📄 README.md                         # File ini

💾 Output Files
all_features.csv - Semua fitur dalam format CSV
features_normalized.csv - Fitur yang sudah dinormalisasi (recommended untuk ML)
features.npy - Fitur dalam format NumPy array
scaler.pkl - Scaler untuk normalisasi data baru
feature_names.txt - Daftar semua nama fitur

HASIL DAN PEMBAHASAN
Dengan total 2.156 fitur per gambar, sistem diharapkan mampu mencapai akurasi klasifikasi yang tinggi untuk 7 kelas senjata yang berbeda.

KESIMPULAN
Implementasi multi-feature approach menunjukkan potensi yang baik untuk klasifikasi objek dalam game computer vision.

⚠️ Troubleshooting
Error GLCM: Sudah difix di program
Error Zernike Moments: Diganti dengan shape features alternatif
Memory Error: CNN features dimatikan untuk optimasi memory

📞 Kontak
Jika ada pertanyaan, hubungi:
Email: [rizkijailani05@gmail.com]
Kelas: [05TPLP004]

Dibuat untuk memenuhi Tugas 4 Machine Learning
Universitas Pamulang  - 2025
```
