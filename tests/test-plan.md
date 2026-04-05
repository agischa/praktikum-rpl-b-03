Test Plan - Aplikasi E-Wallet

1. Rencana Testing Awal
Tujuannya adalah memastikan alur pencatatan pengeluaran dan pemisahan dana (brankas) berfungsi secara logika sebelum masuk ke tahap produksi.

2. Apa yang akan diuji
    Fitur Tracking & Analisis (E-Wallet):
    - Input Pengeluaran: Memastikan saldo E-Wallet berkurang otomatis saat user memasukkan nominal pengeluaran.
    - Kategorisasi: Menguji apakah sistem benar dalam mengelompokkan pengeluaran (misal: Makan, Transport) ke dalam diagram persentase.
    - Akurasi Data: Memastikan total persentase pengeluaran selalu berjumlah 100%.

    Fitur Brankas Tabungan (Inspo: Kantong Jago)
    - Alokasi Dana: Menguji proses pemindahan saldo dari "Saldo Utama" ke "Brankas Khusus" (Nikah, Umroh, dll).
    - Isolasi Saldo: Memastikan saldo yang sudah masuk ke Brankas tidak ikut terpotong saat melakukan transaksi di fitur E-Wallet utama.
    - Target Tabungan: Memastikan ada indikator progres (misal: sudah terkumpul 50%) saat saldo brankas bertambah.