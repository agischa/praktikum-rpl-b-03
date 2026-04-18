Test Plan -Pocket-Mon

1. Rencana Testing
Memastikan seluruh alur keuangan (income, expense, transfer) dan fitur pemisahan dana (multi account, brankas) berjalan dengan presisi dan valid.

2. Fitur yang diuji:
    a. Transaksi (income dan expense)
        - Memastikan saat input pemasukan, saldo pada rekening yang dipilih bertambah secara akurat.
        - Memastikan saat input pengeluaran, saldo pada rekening yang dipilih berkurang secara akurat.
        - Memastikan pengeluaran tidak bisa melebihi sisa saldo.
    
    b. Multi rekening
        - Memastikan setiap rekening memiliki saldo tersendiri dan tidak bercampur.
        - Memastikan transaksi yang dilakukan hanya mempengaruhi rekening yang dipilih oleh user.

    c. Transfer antar rekening
        - Memastikan saldo rekening asal berkurang dan saldo rekening tujuan bertambah dengan jumlah yang sama.
        - Memastikan transaksi transfer tidak masuk ke dalam grafik pengeluaran (karena hanya perpindahan dana)

    d. Kategori dan grafik
        - Memastikan setiap pengeluaran masuk ke kategori yang benar (misal: makan, transport).
        - Grafik harus menampilkan persentase pengeluaran per kategori dengan total akumulasi tepat 100%.

    e. Fitur brankas
        - Menguji pemindahan saldo dari rekening utama ke brankas sesuai target.
        - Memastikan saldo Brankas tetap utuh dan tidak terpengaruh oleh transaksi pengeluaran/pemasukan rutin di akun utama.
        - Memastikan bar progres tabungan bergerak sesuai dengan rasio saldo saat ini dibanding target.
