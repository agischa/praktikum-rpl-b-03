# Data Dictionary — Pocket-Mon

Dokumentasi lengkap kolom untuk setiap entitas pada database aplikasi Pocket-Mon.

---

## Tabel: users

| Kolom | Tipe Data | Constraint | Keterangan |
|-------|-----------|------------|------------|
| id | INT | PK, AUTO_INCREMENT | ID unik pengguna |
| name | VARCHAR(100) | NOT NULL | Nama lengkap pengguna |
| email | VARCHAR(255) | UNIQUE, NOT NULL | Email pengguna, digunakan untuk login |
| password | VARCHAR(255) | NOT NULL | Password pengguna (di-hash dengan bcrypt) |
| created_at | TIMESTAMP | NOT NULL, DEFAULT CURRENT_TIMESTAMP | Waktu akun dibuat |

---

## Tabel: accounts

| Kolom | Tipe Data | Constraint | Keterangan |
|-------|-----------|------------|------------|
| id | INT | PK, AUTO_INCREMENT | ID unik rekening |
| user_id | INT | FK → users.id, NOT NULL | Referensi ke pengguna pemilik rekening |
| name | VARCHAR(100) | NOT NULL | Nama rekening (contoh: Cash, BCA, BRI) |
| type | VARCHAR(50) | NOT NULL | Jenis rekening (contoh: cash, bank, e-wallet) |
| initial_balance | DECIMAL(15,2) | NOT NULL, DEFAULT 0 | Saldo awal saat rekening dibuat |
| created_at | TIMESTAMP | NOT NULL, DEFAULT CURRENT_TIMESTAMP | Waktu rekening dibuat |

---

## Tabel: categories

| Kolom | Tipe Data | Constraint | Keterangan |
|-------|-----------|------------|------------|
| id | INT | PK, AUTO_INCREMENT | ID unik kategori |
| user_id | INT | FK → users.id, NOT NULL | Referensi ke pengguna pemilik kategori |
| name | VARCHAR(100) | NOT NULL | Nama kategori (contoh: Makan, Transport, Gaji) |
| type | VARCHAR(20) | NOT NULL | Jenis kategori: `income` atau `expense` |

---

## Tabel: transactions

| Kolom | Tipe Data | Constraint | Keterangan |
|-------|-----------|------------|------------|
| id | INT | PK, AUTO_INCREMENT | ID unik transaksi |
| account_id | INT | FK → accounts.id, NOT NULL | Referensi ke rekening yang digunakan |
| category_id | INT | FK → categories.id, NOT NULL | Referensi ke kategori transaksi |
| type | VARCHAR(20) | NOT NULL | Jenis transaksi: `income` atau `expense` |
| amount | DECIMAL(15,2) | NOT NULL | Nominal transaksi |
| note | TEXT | NULL | Catatan tambahan transaksi (opsional) |
| date | DATE | NOT NULL | Tanggal transaksi dilakukan |
| created_at | TIMESTAMP | NOT NULL, DEFAULT CURRENT_TIMESTAMP | Waktu data transaksi dicatat di sistem |

---

## Tabel: transfers

| Kolom | Tipe Data | Constraint | Keterangan |
|-------|-----------|------------|------------|
| id | INT | PK, AUTO_INCREMENT | ID unik transfer |
| user_id | INT | FK → users.id, NOT NULL | Referensi ke pengguna yang melakukan transfer |
| from_account_id | INT | FK → accounts.id, NOT NULL | Referensi ke rekening asal (saldo dikurangi) |
| to_account_id | INT | FK → accounts.id, NOT NULL | Referensi ke rekening tujuan (saldo ditambah) |
| amount | DECIMAL(15,2) | NOT NULL | Nominal yang ditransfer |
| date | DATE | NOT NULL | Tanggal transfer dilakukan |
| note | TEXT | NULL | Catatan tambahan transfer (opsional) |

---

## Tabel: brankas

| Kolom | Tipe Data | Constraint | Keterangan |
|-------|-----------|------------|------------|
| id | INT | PK, AUTO_INCREMENT | ID unik brankas |
| user_id | INT | FK → users.id, NOT NULL | Referensi ke pengguna pemilik brankas |
| name | VARCHAR(100) | NOT NULL | Nama tujuan tabungan (contoh: Umroh, Liburan) |
| target_amount | DECIMAL(15,2) | NOT NULL | Nominal target yang ingin dicapai |
| created_at | TIMESTAMP | NOT NULL, DEFAULT CURRENT_TIMESTAMP | Waktu brankas dibuat |

---

## Tabel: brankas_details

| Kolom | Tipe Data | Constraint | Keterangan |
|-------|-----------|------------|------------|
| id | INT | PK, AUTO_INCREMENT | ID unik record alokasi dana ke brankas |
| brankas_id | INT | FK → brankas.id, NOT NULL | Referensi ke brankas tujuan alokasi |
| account_id | INT | FK → accounts.id, NOT NULL | Referensi ke rekening asal alokasi dana |
| amount | DECIMAL(15,2) | NOT NULL | Nominal dana yang dialokasikan ke brankas |

---

## Ringkasan Relasi Antar Tabel

| Tabel Asal | Kolom FK | Tabel Referensi | Kardinalitas | Keterangan |
|------------|----------|-----------------|--------------|------------|
| accounts | user_id | users.id | N:1 | Satu user memiliki banyak rekening |
| categories | user_id | users.id | N:1 | Satu user memiliki banyak kategori |
| transactions | account_id | accounts.id | N:1 | Satu rekening memiliki banyak transaksi |
| transactions | category_id | categories.id | N:1 | Satu kategori dipakai di banyak transaksi |
| transfers | user_id | users.id | N:1 | Satu user dapat melakukan banyak transfer |
| transfers | from_account_id | accounts.id | N:1 | Rekening asal dapat menjadi sumber banyak transfer |
| transfers | to_account_id | accounts.id | N:1 | Rekening tujuan dapat menerima banyak transfer |
| brankas | user_id | users.id | N:1 | Satu user memiliki banyak brankas |
| brankas_details | brankas_id | brankas.id | N:1 | Satu brankas memiliki banyak riwayat alokasi |
| brankas_details | account_id | accounts.id | N:1 | Satu rekening dapat dipakai untuk alokasi ke banyak brankas |
