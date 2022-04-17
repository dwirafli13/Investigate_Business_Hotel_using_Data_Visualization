# Investigate Business Hotel using Data Visualization
Berperan sebagai anggota dari tim Data Scientist yang di berikan tugas untuk memberikan insight yang berhubungan dengan performa bisnis hotel :
- Bagaimana perilaku pelanggan dalam memesan tiket hotel
- Mencari faktor-faktor yang mempengaruhi pembatalan pesanan tiket hotel
## Data Preprocessing
Langkah-langkah yang dilakukan antara lain sebagai berikut :
- Cek kesesuaian tipe data dan cek apakah ada data yang null atau tidak:
  - Untuk semua tipe data sudah sesuai
  - Untuk data yang _null_ saya melakukan proses sebagai berikut :
    - Menghapus kolom `agent` dan kolom `company` karena jumlah data yang null terlalu banyak
    - Mengisi nilai null pada kolom `city` dengan value _unknown_ karena tidak diketahui asal kota customer berasal
    - Menganggap nilai null pada kolom `children` berarti tidak ada tamu anak kecil. Oleh karena itu diisi dengan nilai _0(Zero)_
- Mengganti value _Undefinied_ menjadi _No Meal_ pada kolom `meal` karena sebetulnya artinya sama
- Menghapus data dengan jumlah tamu yang 0(zero)
## Monthly Hotel Booking Analysis Based on Hotel Type
![Monthly Hotel Booking Analysis Based on Hotel Type](https://user-images.githubusercontent.com/99067834/163712038-26ce9069-6e36-489d-8eec-5a3d40c5b942.png)
- Untuk kedua hotel baik _City Hotel_ maupun _Resort Hotel_ memiliki pengungjung yang lebih banyak pada saat musim liburan
- _City Hotel_ memiliki lebih banyak pengunjung di bandingkan dengan _Resort Hotel_
- _City Hotel_ mengalami penurunan jumlah pengungjung yang drastis pada rentang bulan Agustus-September
## Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates
![Impact Analysis of Stay Duration on Hotel Bookings Cancellation Rates](https://user-images.githubusercontent.com/99067834/163712173-4d36c124-80d8-4f14-b323-db0e758027b0.png)
- Semakin lama total malam pada pesanan tamu, maka persentase di batalkannya pesanan juga akan semakin tinggi
- _City Hotel_ memiliki tren yang lebih curam jika di bandingkan dengan _Resort Hotel_
## Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate
![Impact Analysis of Lead Time on Hotel Bookings Cancellation Rate](https://user-images.githubusercontent.com/99067834/163712228-18bf62d6-08ca-4674-9b4c-012d01dc00dc.png)
- Kedua hotel, baik _City Hotel_ maupun _Resort Hotel_ memiliki rasio pembatalan yang paling rendah pada Lead Time 1 Bulan
- Pada Lead Time sekitar 1 Tahun, _Resort Hotel_ memiliki rasio pembatalan yang cukup stagnan yaitu sekitar 40%, sedangkan _City Hotel_ memiliki rasio pembatalan yang cukup tinggi yaitu diatas 60%
