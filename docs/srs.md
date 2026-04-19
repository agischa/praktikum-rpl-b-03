# Software Requirements Specification (SRS

## 1. Pendahuluan

### 1.1 Tujuan Dokumen
Dokumen *Software Requirements Specification (SRS)* ini disusun untuk mendeskripsikan kebutuhan sistem dari aplikasi **Pocket-Mon**, yaitu sebuah aplikasi *financial tracker* yang membantu pengguna dalam mengelola keuangan pribadi. Dokumen ini menjadi acuan bagi tim pengembang dalam proses perancangan, pengembangan, dan pengujian sistem agar sesuai dengan kebutuhan pengguna.

### 1.2 Ruang Lingkup Sistem
**Pocket-Mon** merupakan aplikasi manajemen keuangan yang memungkinkan pengguna untuk:
- Mencatat pemasukan dan pengeluaran
- Mengelola saldo dari berbagai akun
- Melakukan transfer antar akun
- Mengalokasikan dana ke dalam fitur *brankas* (tujuan keuangan)
- Melihat ringkasan kondisi keuangan

Aplikasi ini dirancang untuk membantu pengguna dalam mengontrol arus kas secara terstruktur, memantau perkembangan keuangan, serta mencapai tujuan finansial dengan lebih efektif.

### 1.3 Definisi, Akronim, dan Istilah
Berikut beberapa istilah yang digunakan dalam dokumen ini:

- **User Story (US)**: Deskripsi kebutuhan sistem dari sudut pandang pengguna  
- **FR (Functional Requirement)**: Kebutuhan fungsional sistem yang harus dipenuhi  
- **NFR (Non-Functional Requirement)**: Kebutuhan non-fungsional seperti performa, keamanan, dan kegunaan  
- **Account**: Sumber penyimpanan uang (misalnya rekening bank atau e-wallet)  
- **Transaction**: Aktivitas pemasukan atau pengeluaran uang  
- **Brankas**: Fitur untuk mengalokasikan dana ke dalam tujuan tertentu (misalnya tabungan atau target)  
- **Balance**: Jumlah saldo yang dimiliki pengguna pada suatu akun  
- **Transfer**: Pemindahan saldo dari satu akun ke akun lainnya  ## 1. Pendahuluan

## 2. Deskripsi Umum
(Wawa)
Sistem yang akan dikembangkan merupakan aplikasi manajemen keuangan pribadi berbasis mobile yang memungkinkan pengguna untuk mencatat pemasukan dan pengeluaran secara manual. Sistem ini tidak terhubung langsung dengan layanan perbankan, sehingga seluruh data keuangan diinput secara mandiri oleh pengguna.

Aplikasi ini mendukung pengelolaan keuangan melalui beberapa fitur utama, yaitu manajemen multi rekening (seperti uang tunai dan rekening bank), pencatatan transaksi pemasukan dan pengeluaran, serta fitur transfer antar rekening untuk mengatur distribusi saldo.

Selain itu, sistem menyediakan fitur "Brankas" sebagai media tabungan berbasis tujuan (goal-based saving), yang memungkinkan pengguna untuk mengalokasikan dana dari rekening ke target tertentu seperti tabungan umroh, liburan, atau kebutuhan lainnya.

Sistem juga menyediakan visualisasi data dalam bentuk grafik untuk membantu pengguna memahami pola pengeluaran dan pemasukan, sehingga dapat meningkatkan kesadaran serta kontrol terhadap kondisi keuangan pribadi.

## 3. Functional Requirements

### FR1 (Wawa)
Sistem harus dapat mencatat pengeluaran dari rekening yang dipilih oleh pengguna, dimana pengguna dapat memasukkan nominal, kategori pengeluaran, serta tanggal transaksi, dan sistem akan secara otomatis mengurangi saldo pada rekening tersebut.

### FR2 (Wawa)
Sistem harus dapat mencatat pemasukan ke rekening yang dipilih oleh pengguna, dimana pengguna dapat memasukkan nominal dan sumber pemasukan, dan sistem akan secara otomatis menambahkan saldo pada rekening tersebut.

### FR3 (Noya)
Sistem harus menyediakan fitur pencarian atau penyaringan riwayat transaksi berdasarkan rentang tanggal tertentu (harian, mingguan, atau bulanan).

### FR4 (Noya)
Sistem harus menampilkan seluruh daftar rekening beserta rincian saldo masing-masing secara lengkap.

### FR5 (Lora)
Sistem harus mampu melakukan mutasi saldo antar rekening secara otomatis tanpa merusak statistik pengeluaran.

### FR6 
Sistem harus dapat menyediakan fitur brankas (goal-based saving) yang memungkinkan pengguna untuk membuat target tabungan, mengalokasikan dana dari rekening ke brankas, serta menampilkan progres pencapaian target.

### FR7
Sistem harus dapat memungkinkan pengguna untuk membuat dan mengelola kategori pengeluaran agar transaksi dapat dikelompokkan dengan jelas.

### FR8
Sistem harus dapat menampilkan visualisasi data pengeluaran dalam bentuk grafik berdasarkan kategori, sehingga pengguna dapat memahami pola pengeluaran.


## 4. Non-Functional Requirements

### NFR1 (Noya)
Sistem harus menjamin bahwa 100% input pada kolom nominal hanya terdiri dari angka dan maksimal satu pemisah desimal, guna menghindari kesalahan kalkulasi pada sistem

### NFR2 (Lora)
Sistem harus memiliki tingkat ketersediaan (uptime) minimal 99.5% setiap bulan, sehingga pengguna dapat mengakses catatan keuangan kapan saja tanpa kendala server down.

### NFR3 (Lora)
Sistem harus menjamin tingkat akurasi perhitungan saldo sebesar 100% (zero error) untuk setiap transaksi pemasukan, pengeluaran, maupun transfer antar rekening.

### NFR4 (Wawa)
Sistem harus memiliki waktu respon maksimal 3 detik untuk setiap permintaan pengguna dalam kondisi normal.

## NFR5 (Wawa)
Sistem harus memastikan data pengguna hanya dapat diakses oleh pengguna yang bersangkutan melalui mekanisme autentikasi (login) yang aman.


## 5. Catatan


- Dokumen ini masih dapat mengalami perubahan sesuai dengan kebutuhan pengembangan.
- Semua anggota tim wajib melakukan revisi jika terdapat masukan saat proses review.
