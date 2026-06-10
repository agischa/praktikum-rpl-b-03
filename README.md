# Praktikum RPL B-03
## Deskripsi
Repository ini digunakan untuk pengerjaan tugas Praktikum Rekayasa Perangkat Lunak (RPL) kelompok B-03. Project yang dikembangkan adalah **Pocketmon** — aplikasi manajemen keuangan pribadi berbasis web.
## Anggota Tim
| Nama | NIM |
|------|-----|
| Marleyn Laura O.V.T | L0124023 |
| Nasywa Rifqia R. | L0124027 |
| Wan Nayyara Y. | L0124033 |
| Agischa Nur A. | L0124035 |

## Status Fitur MVP
| No | Fitur | Status |
|----|-------|--------|
| 1 | Autentikasi & Manajemen Wallet (Must-have #1) | ✅ Done |
| 2 | Transaksi (Pemasukan & Pengeluaran) (Must-have #2) | ✅ Done |
| 3 | Brankas & Laporan Statistik (Must-have #3) | 🔄 In Progress |

## Cara Instalasi
1. Clone repository: `git clone https://github.com/agischa/praktikum-rpl-b-03.git`
2. Masuk ke folder src: `cd praktikum-rpl-b-03/src`
3. Install dependencies: `composer install` dan `npm install`
4. Copy env: `cp .env.example .env` lalu `php artisan key:generate`
5. Sesuaikan database di `.env` (DB_DATABASE, DB_USERNAME, DB_PASSWORD)
6. Jalankan migrasi: `php artisan migrate`
7. Jalankan app: `npm run dev` dan `php artisan serve`
8. Buka `http://localhost:8000`

## Struktur Repository
- `docs/` → dokumentasi: SRS, backlog, user stories, UML, wireframe
- `src/` → source code aplikasi Laravel (Pocketmon)
- `tests/` → file pengujian

## Catatan
Branch utama pengembangan adalah `dev`.
Setiap anggota berkontribusi melalui branch masing-masing dan membuat Pull Request ke `dev`.

