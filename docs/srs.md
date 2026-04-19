# Software Requirements Specification (SRS

## 1. Pendahuluan
( Giska)

Dokumen ini berisi spesifikasi kebutuhan perangkat lunak yang akan dikembangkan oleh tim. 
Tujuan dari SRS ini adalah untuk memberikan gambaran yang jelas mengenai fungsi sistem, 
batasan, serta kebutuhan yang harus dipenuhi agar sistem dapat berjalan dengan baik.

Dokumen ini akan menjadi acuan utama dalam proses pengembangan sistem.


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

### NFR4 (Wawa)
Sistem harus memiliki waktu respon maksimal 3 detik untuk setiap permintaan pengguna dalam kondisi normal.

## NFR5 (Wawa)
Sistem harus memastikan data pengguna hanya dapat diakses oleh pengguna yang bersangkutan melalui mekanisme autentikasi (login) yang aman.


## 5. Catatan


- Dokumen ini masih dapat mengalami perubahan sesuai dengan kebutuhan pengembangan.
- Semua anggota tim wajib melakukan revisi jika terdapat masukan saat proses review.
