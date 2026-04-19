# Software Requirements Specification (SRS

## 1. Pendahuluan
### 1.1 Tujuan Dokumen
Dokumen Software Requirements Specification (SRS) ini disusun untuk mendeskripsikan kebutuhan sistem dari aplikasi Pocket-Mon, yaitu sebuah aplikasi financial tracker yang membantu pengguna dalam mengelola keuangan pribadi. Dokumen ini menjadi acuan utama bagi tim pengembang dalam merancang, membangun, dan menguji sistem agar sesuai dengan kebutuhan pengguna.
### 1.2 Ruang Lingkup Sistem
Pocket-Mon merupakan aplikasi manajemen keuangan yang memungkinkan pengguna untuk mencatat pemasukan dan pengeluaran, memantau saldo dari berbagai akun, serta mengelola alokasi dana untuk tujuan tertentu (brankas). Sistem ini menyediakan fitur seperti pencatatan transaksi harian, pengelolaan multi-akun, transfer saldo antar akun, serta visualisasi data keuangan dalam bentuk ringkasan dan grafik.
### 1.3 Definisi, Akronim, dan Istilah
Berikut beberapa istilah yang digunakan dalam dokumen ini:

User Story (US): Deskripsi kebutuhan sistem dari sudut pandang pengguna
FR (Functional Requirement): Kebutuhan fungsional sistem yang harus dipenuhi
NFR (Non-Functional Requirement): Kebutuhan non-fungsional seperti performa, keamanan, dll
Account: Sumber penyimpanan uang (misalnya rekening bank atau e-wallet)
Transaction: Aktivitas pemasukan atau pengeluaran uang
Brankas: Fitur untuk mengalokasikan dana ke dalam tujuan tertentu (misalnya tabungan atau target)
Balance: Jumlah saldo yang dimiliki pengguna pada suatu akun
Transfer: Pemindahan saldo dari satu akun ke akun lainnya.


## 2. Deskripsi Umum
(Penanggung jawab: Wawa)

[SILAKAN DIISI]


## 3. Functional Requirements

### FR1 (Wawa)
[SILAKAN DIISI]

### FR2 (Wawa)
[SILAKAN DIISI]

### FR3 (Noya)
[SILAKAN DIISI]

### FR4 (Noya)
[SILAKAN DIISI]

### FR5 (Lora)
Sistem harus mampu melakukan mutasi saldo antar rekening secara otomatis tanpa merusak statistik pengeluaran.

### FR6 (Giska)
Sistem harus menyediakan fitur utama yang memungkinkan pengguna untuk menggunakan layanan inti dari aplikasi sesuai tujuan sistem.


## 4. Non-Functional Requirements

### NFR1 (Noya)
[SILAKAN DIISI]

### NFR2 (Lora)
Sistem harus memiliki tingkat ketersediaan (uptime) minimal 99.5% setiap bulan, sehingga pengguna dapat mengakses catatan keuangan kapan saja tanpa kendala server down.

### NFR3 (Lora)
Sistem harus menjamin tingkat akurasi perhitungan saldo sebesar 100% (zero error) untuk setiap transaksi pemasukan, pengeluaran, maupun transfer antar rekening.

### NFR4 (Giska)
Sistem harus memiliki waktu respon maksimal 3 detik untuk setiap permintaan pengguna dalam kondisi normal.


## 5. Catatan


- Dokumen ini masih dapat mengalami perubahan sesuai dengan kebutuhan pengembangan.
- Semua anggota tim wajib melakukan revisi jika terdapat masukan saat proses review.
