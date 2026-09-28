# tugas-algoritma2  
**Nama:** Agesti Rahmi Gusmita 
**Kelas:** 3B 

## A. Analisis Komponen  
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
## B. penyusunan pseudocode  
''' text 
PROGRAM Transaksi TokoBuku  
 // &nbsp; Program otomatisasi transaksi kasir untuk menghitung total pembayaran pelanggan beserta validasi input dan penetapan diskon.  

 DEKLARASI:  
 is_member: boolean  
 jumlah_buku: integer  
 total_awal, presentase_diskon, nominal_diskon, total_bayar: real  

 ALGORITMA:  
 // 1. Input data awal  
 INPUT(is_member)  
 INPUT(jumlah_buku)  
 INPUT(total_awal)  
 
 // 2. Validation loop  
 WHILE (total_awal < 0 or jumlah_buku < 1) DO  
       &emsp; OUPUT ("Error: input tidak valid. total awal harus >= 0 dan jumlah buku harus >= 1.")  
       INPUT (is_member)  
       INPUT (jumlah_buku)  
       INPUT (total_awal)  
ENDWHILE  

// 3. Logika Perhitungan diskon  
IF(is_member == true) THEN  
   IF(total_awal > 200000 AND jumlah_buku >= 3) THEN
       &emsp; persentase_diskon <- 0,15
   ELSE  
        &emsp;persentase_diskon <- 0,10  
   ENDIF  
ELSE  
   IF (total_awal >= 300000) THEN  
         &emsp;persentase_diskon <- 0,00  
   ENDIF  
ENDIF  

// 4. Perhitungan Akhir  
nominal_diskon <- total_awal * persentase_diskon total_bayar <- total_awal - nominal_diskon  

//5. Ouput Data  
OUTPUT ("nominal_diskon: Rp", nominal_diskon)  
OUTPUT ("total_bayar akhir: Rp", total_bayar) 

--- 

## C. Uji Logika/trace Tabel  
### kasus A: is_member = True, total_awal = 2500000, jumlah_buku = 4  
| Langkah | Instruksi/Evaluasi Logika | Nilai Variabel Saat Ini | Hasi Evaluasi kondisi |
| --- | --- | --- | --- |
| 1 | Input **data awal** | is_member=**True,** jumlah_buku**=4,** total_awal**=250k** | - | 
| 2 | While **(total_awal < 0 OR jumlah_buku < 1)** | total_awal**=250k,** jumlah_buku **=4** | False (Loop dilewati) |  
| 3 | IF **(is_member == True)** | is_member **=True** | **True** |  
| 4 | IF **(total_awal > = 200k AND jumlah buku >= 3** | total_awal **=250k,** jumlah_buku **=4** | **True** |  
| 5 | persentase_diskon <- 0.15 | persentase_diskon **=0.15** | - |  
| 6 | nominal_diskon <- total awal * persentase_diskon | nominal_diskon **=37500** | - |  
| 7 | total_bayar <- total_awal - nominal_diskon | total_bayar **212500** | - |  
| 8 | OUTPUT | **Diskon:** 37500, **Total:** 212500 | - | 

### Kasus B: is_member = False, tootal_awal = 350000, jumlah_buku = 2  
| Langkah | Instruksi / Evaluasi Logika | Nilai Varibel Saat Ini | Hasil Evaluasi Kondisi | 
| --- | --- | --- | --- |
| 1 | Input **data** | is_member=**False,** jumlah_buku= **2,** total_awal=**350000** | - | 
| 2 | WIHILE (total_awal < 0 OR jumlah_buku < 1) | total awal=**350k,** julah_buku=**2** | False (loop dilewati) | 
| 3 | IF (is_member === True) | is_member=**False** | False (lompat ke ELSE) | 
| 4 | IF **(Total_awal >== 300000)** | total_awal = **350k** | True | 
| 5 | persentase_diskon <- 0.05 | persentase_diskon=**0.05** | - | 
| 6 | nominal_diskon <- awal persentase_diskon | nominal_diskon=**17500** | - | 
| 7 | total_bayar <- total awal - nominal_diskon | total_bayar=**332500** | - | 
| 8 | OUTPUT | **Diskon:** 17500, **Total:** 332500 | - | 

### Kasus C:Input total_awal = -50000, dikereksi -> 100000, is_member = False, jumlah_buku = 1
| Langkah | Instruksi  / Evaluasi Logika | Nilai Varibel Saat Ini | Hasil Evaluasi Kondisi | 
| --- | --- | --- | --- |
| 1 | Inputg data awal (salah) | is_member=**False,** jumlah_buku=**1,** total_awal= **-50000**  | - | 
| 2 | WHILE (total_awal < 0 OR jumlah_buku < 1) | total_awal= **-50000** | True (Masuk ke Loop) | 
| 3 | OUTPUT **Error &** INPUT **ualang** | total_awal = **100000 (koleksi)** | - | 
| 4 | WHILE **(total_awal < 0 OR jumlah_buku < 1)** | total_awal = **100k,** jumlah_buku = **1** | False (Keluar Loop) | 
| 5 | IF (is_member == True) | is_member=**False** | False (Lompat ke ELSE) | 
| 6 | IF **(total_awal >= 300000)** | total_awal=**100k** |  False (Lompat ke ELSE) | 
| 7 | persentase_diskon <- 0.00 | persentase_diskon=0.00 | - | 
| 8 | nominal_diskon <- total_awal * persentase_diskon | nominal_diskon=0 | -| 
| 9 | total_bayar <- total_awal - nominal_diskon | total_bayar=**100000** | - | 
| 10 | OUTPUT | **Diskon:** 0, **Total:** 100000 | - | 



