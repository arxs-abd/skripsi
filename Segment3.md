# 3. Metode Penelitian

## 3.1 Prosedur Penelitian

Prosedur Penelitian merupakan serangkaian kegiatan yang dilaksanakan secara sistematis serta teratir agar mencapai tujuan dari penelitian ini. Adapun prosedur penelitian sebagai berikut :

1. Analisa Kebutuhan Sistem
   Dalam tahap ini, dilakukan analisa terhadap kebutuhan sebuah sistem seperti bagaimana tampilan sistem, bagaimana cara kerja sistem, ataupun penggunaan bahasa pemrograman yang tepat.
2. Studi Literatur
   Dalam tahap ini, dilakukan pengumpulan teori - teori ataupun landasan dasar dalam proses membangun sebuah sistem yang akan dibuat.
3. Perancangan Sistem
   Dalam tahap ini, dilakukan pembangunan Sistem Pendeteksi Kesamaan Teks Menggunakan Metode Dice Similarity dengan menggunakan metode, teori, ataupun bahasa pemrograma yang telah ditentukan sebelumnya.
4. Pengujian Sistem
   Dalam tahap ini, dilakukan testing atau pengujian terhadap sistem.

## 3.2 Rancangan Sistem

### 3.2.1 Use Case Diagram

Use Case Diagram adalah suatu jenis diagram yang menggambarkan hubungan atau interaksi dari sebuah sistem dengan pengguna. Dengan adanya Use Diagram, kita dapat mendeskripsikan tipe atau jenis yang dilakukan pengguna terhadap sebuah sistem. Berikut use case diagram dari Sistem Pendeteksi Kesamaan Teks Menggunakan Metode Dice Similarity.

![Use Case Diagram](img/use_case.png)

### 3.3.2 ER Diagram

Entity Relationship Diagram (ERD) adalah suatu jenis diagram yang digunakan untuk merancang suatu basis data (database). Dalam ERD, terdapat beberapa komponen seperti entitas, relasi, atribut, dan garis penghubung dimana digunakan untuk memperlihatkan hubungan atau relasi antar entitas atau objek yang terlihat beserta atributnya. Berikut ER diagram dari Sistem Pendeteksi Kesamaan Teks Menggunakan Metode Dice Similarity.

![Entity Relationship Diagram](img/erd.png)

### 3.3.3 Desain Sistem

Pada bagian ini, akan menjelaskan bagaimana desain suatu sistem yang diimplemetasikan. Dengan adanya desain sistem ini, dapat memberikan gambaran rancang bangun yang lengkap terhadap pengguna dari sistem ini.

#### 3.3.3.1 Algoritma Input Teks ke Dalam Database

![Flowchart Input Teks ke Dalam Database](img/flowchart_input.png)

Keterangan :

1. Input Teks
   Sebelum membandingkan teks yang akan ditentukan kesamaannya, terlebih dahulu dibuat sebuah repositori atau database teks yang akan digunakan sebagai pembanding nantinya. Teks yang diinput pada penelitian ini berupa file yang berformat Pdf (Portable Document Format).

2. Konversi Teks
   Teks yang telah diinput, kemudian diubah kedalam bentuk tipe data _String_ agar dapat diolah nantinya didalam sistem.

3. Hapus Stopword
   Stopword merupakan kata yang diabaikan karena memeiliki frekuensi kemunculan yang sangat tinggi dan tidak mempunyai arti. Beberapa contoh Stopw word seperti, "atau", "dan", dan "tapi". Dengan menghapus Stopword, sistem dapat bekerja lebih cepat karena Stopword akan menghapus kata yang abaikan.

4. Hapus Karakter
   Selain Stopword, karakter seperti ",", ".", "?", dll yang hanya berupa karakter yang tidak memiliki arti dan fungsi karena sistem hanya memeriksa kata.

5. Simpan di Database
   Setelah teks telah melewati tahap sebelumnya, maka teks akan dimasukkan kedalam database yang nantinya akan digunakan saat ingin mendapatkan persentase kemiripan dari teks yang akan dibandingkan nantinya.

#### 3.3.3.2 Algoritma Perbandingan Teks

![Flowchart Perbandingan Teks](img/flowchart_check.png)

Keterangan :

1. Input Teks
   Input teks yang akan dibandingkan kedalam sistem yang nantinya akan dibandingkan terhadap teks yang terdapat dalam database atau repositori. Teks yang diinput berupa teks yang berformat Pdf (Portable Document Format).

2. Konversi Teks
   Teks yang telah diinput, kemudian diubah kedalam bentuk tipe data _String_ agar dapat diolah nantinya didalam sistem.

3. Hapus Stopword
   Stopword merupakan kata yang diabaikan karena memeiliki frekuensi kemunculan yang sangat tinggi dan tidak mempunyai arti. Beberapa contoh Stopw word seperti, "atau", "dan", dan "tapi". Dengan menghapus Stopword, sistem dapat bekerja lebih cepat karena Stopword akan menghapus kata yang abaikan.

4. Hapus Karakter
   Selain Stopword, karakter seperti ",", ".", "?", dll yang hanya berupa karakter yang tidak memiliki arti dan fungsi karena sistem hanya memeriksa kata.

5. Hitung Nilai Kemiripan
   Setelah teks melewati tahap sebelumnya, maka teks akan dibandingan dengan semua teks yang terdapat didalam database atau repositori. Teks akan dibandingkan dengan semua data teks dengan menggunakan metode Dice Similarity. Kemudian hasil kemiripan antar teks akan muncul sebanyak data yang terdapat dalam database atau repositori teks.

## 3.3 Metode Penelitian

Dalam sistem ini, metode perhitungan yang digunakan adalam metode Dice Similarity dengan membandingkan data teks yang diinput pengguna dengan teks yang terdapat didalam database atau repositori teks. Algoritma perhitungan persentase kemiripan antar teks sebagai berikut :

![Flowchart Dice Similarity](img/algo_dice_similarity.png)

## 3.3 Instrumen Penelitian

Instrumen yang digunakan dalam penelitian ini adalah laptop dengan processor AMD Athlon 300U with Radeon Vega Mobile Gfx 2.40 GHz dan RAM sebanyak 8 GB serta sistem operasi windows 10 Home 64 bit.
