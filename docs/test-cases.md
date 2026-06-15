# Test Cases — Pocket-Mon (Praktikum P9)

**Aplikasi diuji:** https://pocketmon-production.up.railway.app/
**Kelompok:** Wawa, Noya, Giska, Lora
**Tanggal eksekusi:** Minggu, 14 Juni 2026

## Environment

| Anggota | OS | Browser (isi versi) |
|---------|----|--------------------|
| Wawa | Windows | Chrome _(v149)_ |
| Noya | Windows | Chrome _(v149)_ |
| Lora | Windows | Chrome _(v149)_ |
| Giska | Linux Ubuntu | Chrome _(v149)_ |

## Pembagian Penulisan & Cross-Testing

> Aturan: **penguji ≠ penulis fitur** (cross-testing untuk perspektif segar).

| Anggota | Menulis test case | Meng-eksekusi (cross-test) |
|---------|-------------------|----------------------------|
| Wawa | TC001–TC005 (Autentikasi & Tamu) | TC006–TC010 (Transaksi) |
| Noya | TC006–TC010 (Transaksi) | TC011–TC014 (Wallet & Transfer) |
| Giska | TC011–TC014 (Wallet & Transfer) | TC015–TC021 (Dashboard, Filter, Brankas, Laporan) |
| Lora | TC015–TC021 (Dashboard, Filter, Brankas, Laporan) | TC001–TC005 (Autentikasi & Tamu) |

## Petunjuk Eksekusi
1. Jalankan tiap test case **berurutan**, ikuti Steps persis.
2. Isi kolom **Actual Result** apa adanya (bukan yang diharapkan).
3. Tandai **Status**: `Pass` jika Actual = Expected, `Fail` jika berbeda.
4. Setiap baris **Fail** → buat GitHub Issue berlabel `bug` (lihat format di bawah) + screenshot.

---

## Daftar Test Case

| TC-ID | Judul | Precondition | Steps | Expected Result | Actual Result | Status |
|-------|-------|--------------|-------|-----------------|---------------|--------|
| TC001 | Login valid (US-13) | Akun sudah terdaftar; halaman /login terbuka | 1. Buka /login 2. Isi email & password yang benar 3. Klik "Masuk" | Login berhasil, diarahkan ke dashboard, nama/akun user tampil | Login berhasil dilakukan, sistem langsung mengarahkan ke dashboard dan nama user tampil di layar. | Pass |
| TC002 | Login password salah (US-13) | Halaman /login terbuka | 1. Buka /login 2. Isi email benar, password salah 3. Klik "Masuk" | Muncul pesan kredensial salah; tetap di halaman login; tidak masuk dashboard | Sistem memunculkan pesan error kredensial salah, pengguna tetap berada di halaman login dan tidak masuk ke dashboard. | Pass |
| TC003 | Login input tidak valid (US-13) | Halaman /login terbuka | 1. Buka /login 2. Kosongkan email & password (atau isi email tanpa "@") 3. Klik "Masuk" | Muncul validasi field wajib / format email tidak valid; form tidak terkirim | Sistem menampilkan pesan validasi field wajib/format tidak valid, dan form gagal dikirim. | Pass |
| TC004 | Register akun baru valid (US-13) | Halaman /register terbuka; email belum terdaftar | 1. Buka /register 2. Isi nama, email baru valid, password & konfirmasi 3. Klik "Daftar" | Akun berhasil dibuat, user diarahkan ke dashboard/login | Akun baru berhasil didaftarkan, pengguna langsung diarahkan ke halaman login/dashboard. | Pass |
| TC005 | Masuk sebagai Tamu (US-11) | Berada di halaman landing | 1. Klik "Coba Sebagai Tamu" (/guest) 2. Konfirmasi peringatan data lokal (jika ada) | Tanpa login, diarahkan ke setup wallet / dashboard mode tamu | Pengguna berhasil masuk tanpa login dan langsung diarahkan ke halaman setup wallet mode tamu. | Pass |
| TC006 | Tambah pemasukan valid (US-01) | Sudah login; punya minimal 1 wallet | 1. Buka form Tambah Pemasukan 2. Isi nominal, kategori, pilih wallet tujuan 3. Simpan | Saldo wallet bertambah sesuai nominal; transaksi tercatat di riwayat | Saldo wallet tujuan bertambah sesuai nominal pemasukan, dan transaksi berhasil tercatat di riwayat. | Pass |
| TC007 | Pemasukan nominal tidak valid (US-01) | Sudah login | 1. Buka form pemasukan 2. Kosongkan nominal (atau isi 0 / angka negatif) 3. Simpan | Muncul validasi nominal harus lebih dari 0; data tidak tersimpan; saldo tidak berubah | Muncul pesan peringatan nominal tidak valid, data pemasukan ditolak, dan saldo tetap tidak berubah. | Pass |
| TC008 | Tambah pengeluaran valid (US-09) | Sudah login; wallet punya saldo cukup | 1. Buka form Tambah Pengeluaran 2. Isi nominal, kategori, pilih wallet sumber 3. Simpan | Saldo wallet berkurang sesuai nominal; transaksi tercatat di riwayat | Saldo wallet sumber berkurang sesuai nominal pengeluaran, dan transaksi tercatat di riwayat dengan benar. | Pass |
| TC009 | Pengeluaran melebihi saldo (US-09) | Sudah login; saldo wallet lebih kecil dari nominal | 1. Buka form pengeluaran 2. Isi nominal > saldo wallet 3. Simpan | Sistem menolak / beri peringatan saldo tidak cukup; saldo tidak menjadi minus | Sistem memberikan peringatan bahwa saldo tidak cukup, transaksi gagal disimpan, dan saldo tidak menjadi minus. | Pass |
| TC010 | Edit transaksi & penyesuaian saldo (US-04) | Ada transaksi tersimpan | 1. Buka detail transaksi 2. Ubah nominal/kategori 3. Klik Simpan | Data ter-update, muncul notifikasi sukses, saldo wallet menyesuaikan otomatis | Data transaksi berhasil diperbarui, muncul notifikasi sukses, dan saldo wallet langsung menyesuaikan otomatis. | Pass |
| TC011 | Tambah wallet baru valid (US-10) | Sudah login; di halaman wallet/akun | 1. Klik "Tambah Wallet" 2. Isi nama, tipe, saldo awal 3. Simpan | Wallet baru dibuat & muncul di daftar; tersedia sebagai sumber/tujuan transaksi | Wallet baru berhasil ditambahkan, muncul di daftar wallet, dan bisa dipilih untuk transaksi selanjutnya. | Pass |
| TC012 | Tambah wallet nama kosong (US-10) | Sudah login | 1. Klik "Tambah Wallet" 2. Kosongkan nama 3. Simpan | Muncul validasi nama wajib diisi; wallet tidak dibuat | Sistem menampilkan pesan validasi bahwa nama wallet wajib diisi, dan pembuatan wallet dibatalkan. | Pass |
| TC013 | Transfer antar wallet valid (US-12) | Sudah login; punya ≥2 wallet, sumber saldo cukup | 1. Buka menu Transfer 2. Isi nominal, pilih wallet sumber & tujuan (berbeda) 3. Simpan | Saldo sumber berkurang, tujuan bertambah; dicatat sebagai Transfer (bukan pengeluaran) | Saldo berhasil berpindah dengan benar, namun transaksi tersebut sama sekali tidak tercatat di halaman Riwayat. | Fail |
| TC014 | Transfer tidak valid (US-12) | Sudah login | 1. Buka Transfer 2. Pilih sumber = tujuan (atau nominal > saldo) 3. Simpan | Sistem menolak; muncul pesan error; saldo tidak berubah | Sistem menolak transaksi transfer, memunculkan pesan error, dan saldo kedua wallet tidak mengalami perubahan. | Pass |
| TC015 | Total saldo gabungan di dashboard (US-02) | Sudah login; beberapa wallet berisi saldo | 1. Buka dashboard 2. Amati "Total Saldo" | Total saldo = penjumlahan saldo semua wallet aktif, nilainya benar | Dashboard menampilkan total saldo gabungan dengan nilai kalkulasi yang tepat dari seluruh wallet aktif. | Pass |
| TC016 | Filter riwayat by rentang tanggal (US-03) | Sudah login; ada transaksi di berbagai tanggal | 1. Buka Riwayat 2. Pilih tanggal mulai & akhir 3. Terapkan filter | Hanya transaksi dalam rentang tanggal tersebut yang ditampilkan | Riwayat transaksi berhasil difilter dan hanya menampilkan data yang sesuai dengan rentang tanggal yang dipilih. | Pass |
| TC017 | Filter tanggal akhir lebih awal dari mulai (US-03) | Sudah login; di halaman Riwayat | 1. Buka Riwayat 2. Set tanggal akhir < tanggal mulai 3. Terapkan | Sistem memberi validasi / hasil kosong yang wajar (tidak error/crash) | Sistem menampilkan daftar riwayat kosong secara normal tanpa terjadi error atau crash pada aplikasi. | Pass |
| TC018 | Alokasi saldo ke Brankas valid (US-06) | Sudah login; saldo wallet cukup; ada Brankas | 1. Buka Brankas 2. Pilih Brankas, isi nominal alokasi 3. Simpan | Saldo wallet berkurang, saldo Brankas bertambah sesuai nominal | Saldo terkumpul di Brankas bertambah sesuai nominal, namun saldo wallet utama tidak berkurang sama sekali. | Fail |
| TC019 | Brankas terkunci dari pengeluaran (US-07) | Sudah login; ada Brankas berisi saldo | 1. Buka form pengeluaran 2. Periksa daftar pilihan wallet sumber | Saldo/akun Brankas tidak bisa dipilih/terkunci sebagai sumber pengeluaran harian | Pengujian diblokir (Blocked). Fitur ini tidak dapat diverifikasi dengan valid karena terhalang oleh kegagalan sistem (bug) pada alokasi dana di TC018. | Blocked |
| TC020 | Progress tabungan Brankas (US-08) | Sudah login; Brankas punya target & sebagian terisi | 1. Buka detail Brankas | Tampil progress bar / persentase terkumpul vs target dengan nilai yang benar | Progress bar dan persentase tabungan terkumpul tampil dengan akurat sesuai dengan perhitungan target. | Pass |
| TC021 | Grafik kategori pengeluaran (US-05) | Sudah login; ada beberapa pengeluaran berkategori | 1. Buka halaman Laporan/Statistik | Tampil grafik (pie/bar) yang menunjukkan persentase pengeluaran per kategori | Halaman laporan hanya menampilkan rincian pengeluaran per kategori dalam bentuk daftar teks biasa tanpa visualisasi grafik (pie/bar) maupun persentase. | Fail |

---

## Ringkasan Eksekusi (isi setelah selesai)

- Total test case: **21**
- Pass: **17**
- Fail: **3**
- Bug ditemukan: **3**
- Blocked: **1**

## Daftar Bug (isi link GitHub Issue)

| TC Gagal | Bug Issue | Severity |
|----------|-----------|----------|
| TC013 | *https://github.com/agischa/praktikum-rpl-b-03/issues/35#issue-4666100632* | High |
| TC018 | *https://github.com/agischa/praktikum-rpl-b-03/issues/33#issue-4665750575* | High |
| TC021 | *https://github.com/agischa/praktikum-rpl-b-03/issues/34#issue-4665829649* | Medium |