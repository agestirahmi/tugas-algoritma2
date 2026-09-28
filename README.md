# tugas-algoritma2  
## Analisis Komponen  
### 1. Identifikasi Variabel  
| No | Varial | Tipe Data | keterangan |  
|--- | --- | --- | ---- |
| 1 | is_member | Boolean | Menyimpan status pelanggan, yaitu member atau bukan member. |  
| 2 | jurnal_buku | Integer | Menyimpan buku yang dibeli. |  
| 3 | total_awal | Real | Menyimpan total belanja sebelum didiskon. |  
| 4 | diskon_persen | Real | Menyimpan persentase diskon yang diperoleh. |  
| 5 | nominal_diskon | Real | Menyimpan jumlah uang yang dipotong sebagai diskon. |  
| 6 | total_ bayar | Real | Menyimpan total yang harus dibayar setelah diskon. |  

### 2. Struktur kontrol yang digunakan  
| Struktur Kontrol | digunakan untuk |  
| --- | --- |
| Sequence | ketika program menjakankan langkah secara berurutan, misalnya membaca input, menghitung nominal diskon, lalu menghitung total bayar |  
| Selection | untuk menentukan diskon berdasarkan status member, jumlah buku, dan total belajar. Bentuk yang digunakan pelanggan member terdapat percadangan bertingkat (nested IF).  |  
| literation | pada proses Validasi. Jika total_awal < 0 atau jumlah_buku < 1 , data memasukan data kembali. pengulangan berhenti setelah semua data vlid. |  
## pseudocode  
PROGRAM Transaksi TokoBuku  
 Program otomatisasi transaksi kasir untuk menghitung total pembayaran pelanggan beserta validasi input dan penetapan diskon.



