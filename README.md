# Tugas 8 MySQL
Silahkan teman-teman buat table tugas_populasi di dalam database belajar. Struktur serta isi data tabel disamakan dengan gambar diatas. Jika sudah, silahkan kerjakan tugas berikut:

![Tugas 8.1](https://github.com/troy213/tugas_8_mysql/blob/main/Tugas%208.1.png)

#### 1. Tampilkan kolom kota, kec, luas dan penduduk!
```
SELECT kota, kec, luas, penduduk FROM populasi;
```

#### 2. Tampilkan kolom kota kemudian ubah namanya menjadi Nama Kota, kolom kec menjadi Jumlah Kecamatan dan kolom kel menjadi Jumlah Kelurahan!
```
SELECT kota AS 'Nama Kota', kec AS 'Jumlah Kecamatan', kel AS 'Jumlah Kelurahan' FROM populasi;
```

#### 3. Tampilkan data dari table tugas_populasi berdasarkan Kecamatan dari jumlah terbesar!
```
SELECT * FROM populasi ORDER BY kec DESC;
```

#### 4. Urutkan berdasarkan kolom kel lalu diambil 5 data setelah baris ke-2!
```
SELECT * FROM populasi ORDER BY kel ASC LIMIT 2,5;
```

#### 5. Tampilkan data dimana kolom kota berisi string Depok!
```
SELECT * FROM populasi WHERE kota LIKE 'Depok';
```

Perhatikan gambar dibawah ini!

![Tugas 8.2](https://github.com/troy213/tugas_8_mysql/blob/main/Tugas%208.2.png)

Silahkan teman-teman buat table tugas_daftar_provinsi di dalam database belajar. Struktur serta isi data tabel disamakan dengan gambar diatas. Jika sudah, silahkan kerjakan tugas berikut:

#### 6. Tuliskan query untuk menampilkan hasil berikut

![Tugas 8.3](https://github.com/troy213/tugas_8_mysql/blob/main/Tugas%208.3.png)

**Note: Gunakan query SELECT… WHERE table tugas_provinsi = tugas_daftar_provinsi**
```
SELECT provinsi.prov, populasi.kota, populasi.penduduk FROM provinsi, populasi WHERE provinsi.ibukota = populasi.kota;
```

#### 7. Tampilkan isi tabel populasi dimana nilai kolom kecamatan antara 20 dan 30!
```
SELECT * FROM populasi WHERE kec BETWEEN 20 AND 30;
```
