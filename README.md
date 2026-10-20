# UTS_Graf_Sains_Data_026_Naza_SW

Pengerjaan UTS Graf Sains Data 2026/2027 menggunakan dataset RetailRocket, Neo4j, analisis similarity, dan sistem rekomendasi KNN.

**Nama:** Naza Sulthoniyah Wahda  
**NIM:** 23026  
**Mata Kuliah:** Graf Sains Data  
**Program Studi:** Sains Data, Universitas Negeri Surabaya

## Deskripsi Proyek

Repository ini berisi pengerjaan Ujian Tengah Semester (UTS) mata kuliah Graf Sains Data. Pengerjaan meliputi pengolahan dataset RetailRocket, implementasi graf menggunakan Neo4j, analisis similarity, dan sistem rekomendasi menggunakan K-Nearest Neighbors (KNN).

## Isi Repository

- Notebook: implementasi dan analisis pengerjaan UTS.
- `requirements.txt`: daftar library Python yang diperlukan.
- `data/`: dataset yang digunakan dalam pengerjaan dan data hasil pemrosesan.
- `image/`: dokumentasi proses pengerjaan dan hasil visualisasi.

## Dataset

Dataset yang digunakan adalah RetailRocket E-commerce Dataset yang diperoleh dari Kaggle.

**Sumber dataset:**  
https://www.kaggle.com/api/v1/datasets/download/retailrocket/ecommerce-dataset

### 1. Tugas Pendahuluan

Berkas `events.csv` merupakan dataset interaksi pengguna dengan produk yang digunakan untuk memeriksa atribut data dan melakukan proses impor data ke Neo4j.

Atribut utama pada dataset `events.csv` meliputi:

- `timestamp`: waktu kejadian dalam format Unix epoch.
- `visitorid`: ID unik pengunjung.
- `event`: jenis interaksi, seperti `view`, `addtocart`, dan `transaction`.
- `itemid`: ID unik produk.
- `transactionid`: ID transaksi yang terisi pada kejadian transaksi.

### 2. Pengerjaan Soal UTS

Dataset interaksi dibagi berdasarkan periode waktu untuk keperluan training dan testing sistem rekomendasi.

- `events_P1_2015-08.csv`: data training periode 1–31 Agustus 2015.
- `events_P2_2015-09_01-14.csv`: data testing periode 1–14 September 2015.

Pembagian periode menggunakan batas awal inklusif dan batas akhir eksklusif.

### 3. Cara Mengunduh Dataset

Dataset asli dapat diunduh melalui tautan Kaggle di atas.

Pada Windows PowerShell, jalankan:

```powershell
cd "$env:USERPROFILE\Downloads"

curl.exe -L -o ecommerce-dataset.zip https://www.kaggle.com/api/v1/datasets/download/retailrocket/ecommerce-dataset
```

Setelah unduhan selesai, ekstrak dataset menggunakan:

```powershell
Expand-Archive -Path "$env:USERPROFILE\Downloads\ecommerce-dataset.zip" -DestinationPath "$env:USERPROFILE\Downloads\retailrocket" -Force
```

Dataset asli mencakup berkas `category_tree.csv`, `events.csv`, `item_properties_part1.csv`, dan `item_properties_part2.csv`.

Berkas `events.csv` serta kedua berkas `item_properties` tidak disertakan dalam repository karena pertimbangan ukuran berkas. Berkas yang tidak disertakan dapat diunduh dari sumber dataset asli sesuai kebutuhan pengerjaan.

## Menjalankan Notebook

1. Clone repository ini.
2. Siapkan environment Python.
3. Instal dependensi menggunakan `requirements.txt`.
4. Pastikan dataset yang diperlukan tersedia.
5. Sesuaikan path dataset dengan lokasi berkas pada komputer.
6. Jalankan notebook secara berurutan.

## Dokumentasi

Bukti pengerjaan dan visualisasi graf tersedia pada folder `image/`.
