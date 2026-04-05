# ☁️ Ekstraksi Fitur Warna Citra Langit (Computer Vision)

Repository ini berisi *source code* dan dokumentasi untuk tugas mata kuliah **Computer Vision**. Proyek ini bertujuan untuk melakukan ekstraksi fitur warna pada citra langit dan mengklasifikasikan kondisi cuaca secara otomatis menggunakan algoritma *thresholding* berbasis Python dan OpenCV

## 🔗 Tautan Penting

* 📂 **Dataset Citra :** https://drive.google.com/drive/folders/1pQ7XJyZw5hZCkAvnXq0bWv0isATVb1tg?usp=sharing
* 🐍 **Google Colab :** https://colab.research.google.com/drive/1nbQPP62bqld_MX_HYRm6M3iAqTRNqT7O?usp=sharing

---

## 📌 Deskripsi Proyek

Sistem ini tidak bergantung pada waktu/jam pengambilan gambar, melainkan murni menganalisis komposisi piksel warna citra (RGB) untuk mendeteksi fenomena atmosfer nyata

Terdapat 4 kategori klasifikasi cuaca pada sistem ini :
1. ☀️ **Langit Cerah (Clear Sky)**
2. 🌤️ **Berawan (Cumulus)**
3. 🌫️ **Mendung (Nimbostratus)**
4. 🌅 **Senja (Sunset)**

## 🧮 Logika Klasifikasi (Parameter)

Sistem menggunakan **Nilai Rata-rata (Mean)** dari setiap kanal warna (Red, Green, Blue). Dari nilai tersebut, dibuat dua parameter utama :
1. **Total RGB** = `Mean R + Mean G + Mean B` (Untuk mengukur intensitas cahaya/Albedo).
2. **Rasio R/B** = `Mean R / Mean B` (Untuk mendeteksi efek Hamburan Rayleigh).

**Aturan Thresholding:**
* **Senja :** `Rasio R/B >= 1.5` (Warna merah sangat dominan).
* **Mendung :** `Rasio R/B >= 0.81` DAN `Total RGB < 400` (Warna netral/abu-abu dan minim cahaya).
* **Langit Cerah :** `Rasio R/B < 0.45` (Warna biru sangat dominan).
* **Berawan :** Nilai sisa dari rentang di atas (Cerah dengan pantulan awan putih).

## 🛠️ Teknologi yang Digunakan
* **Python 3**
* **OpenCV** (`cv2`) - *Preprocessing* dan konversi BGR ke RGB
* **NumPy** - Perhitungan matriks dan *Mean* warna
* **Pandas** - Pembuatan DataFrame dan penyimpanan ke format CSV
* **Matplotlib** - Visualisasi citra dataset

## 🚀 Cara Penggunaan
1. Buka tautan Google Colab yang tersedia di atas.
2. Pastikan Anda memiliki akses ke folder Dataset di Google Drive.
3. *Run all cells* pada *notebook* untuk melihat hasil visualisasi citra, ekstraksi tabel klasifikasi, dan *output* file `.csv`.
