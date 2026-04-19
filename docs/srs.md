# Software Requirements Specification (SRS

## 1. Pendahuluan
( Giska)

Dokumen ini berisi spesifikasi kebutuhan perangkat lunak yang akan dikembangkan oleh tim. 
Tujuan dari SRS ini adalah untuk memberikan gambaran yang jelas mengenai fungsi sistem, 
batasan, serta kebutuhan yang harus dipenuhi agar sistem dapat berjalan dengan baik.

Dokumen ini akan menjadi acuan utama dalam proses pengembangan sistem.


## 2. Deskripsi Umum
(Penanggung jawab: Wawa)

[SILAKAN DIISI]


## 3. Functional Requirements

### FR1 (Wawa)
[SILAKAN DIISI]

### FR2 (Wawa)
[SILAKAN DIISI]

### FR3 (Noya)
Sistem harus menyediakan fitur pencarian atau penyaringan riwayat transaksi berdasarkan rentang tanggal tertentu (harian, mingguan, atau bulanan).

### FR4 (Noya)
Sistem harus menampilkan seluruh daftar rekening beserta rincian saldo masing-masing secara lengkap.

### FR5 (Lora)
Sistem harus mampu melakukan mutasi saldo antar rekening secara otomatis tanpa merusak statistik pengeluaran.

### FR6 (Giska)
Sistem harus menyediakan fitur utama yang memungkinkan pengguna untuk menggunakan layanan inti dari aplikasi sesuai tujuan sistem.


## 4. Non-Functional Requirements

### NFR1 (Noya)
Sistem harus menjamin bahwa 100% input pada kolom nominal hanya terdiri dari angka dan maksimal satu pemisah desimal, guna menghindari kesalahan kalkulasi pada sistem

### NFR2 (Lora)
Sistem harus memiliki tingkat ketersediaan (uptime) minimal 99.5% setiap bulan, sehingga pengguna dapat mengakses catatan keuangan kapan saja tanpa kendala server down.

### NFR3 (Lora)
Sistem harus menjamin tingkat akurasi perhitungan saldo sebesar 100% (zero error) untuk setiap transaksi pemasukan, pengeluaran, maupun transfer antar rekening.

### NFR4 (Giska)
Sistem harus memiliki waktu respon maksimal 3 detik untuk setiap permintaan pengguna dalam kondisi normal.


## 5. Catatan


- Dokumen ini masih dapat mengalami perubahan sesuai dengan kebutuhan pengembangan.
- Semua anggota tim wajib melakukan revisi jika terdapat masukan saat proses review.
