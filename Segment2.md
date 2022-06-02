# Rancang Bangun Sistem Mendeteksi Kesamaan Teks Menggunakan Metode N-Grams dan Jaccard Similiratiy

# 2 Tinjauan Pustaka

## 2.1 Penelitian Terkait

- Dalam Penelitian Mufti Ari Bianto, dkk (2018) dengan judul _Perancangan Sistem Pendeteksi Plagiarisme Terhadap Topik Penelitian Menggunakan Metode K-Means Clustering dan Model Bayesian_, hasil kemiripan diuji berdasarkan kesamaan pola kata dalam kalimat, dokumen dengan Nilai similarity tertinggi diperoleh 1 dokumen dengan presentase kemiripan sebanyak 100 %, dan jika berdasarkan kesamaan term, berpengaruh terhadap hasil dokumen mirip yang dihasilkan, sehingga diperoleh 2 dokumen mirip. Meskipun uji berdasarkan kesamaan term, menghasilkan dokumen mirip yang lebih banyak namun belum cukup akurat menunjukkan adanya plagiasi, karena dalam menentukan plagiasi kesamaan rangkaian kalimat merupakan hal yang penting untuk diperhatikan.

- Dalam penelitian Joko Priambodo (2018) dengan judul _Pendeteksian Plagiarisme Menggunakan Algoritma Rabin - Karb dengan Meotde Rolling Hash_, pendeteksian plagiarisme menggunakan algoritma Rabin-Karp dengan metode rolling hash dari hasil pengujian 30 dokumen teks yang sudah dijelaskan pada bab sebelumnya menghasilkan tingkat akurasi yang terbesar yaitu 47.58 %. Hasil persentase tersebut termasuk dalam kategori tingkat plagiat 15 - 50 %, berarti menandakan dokumen tersebut termasuk plagiat tingkat sedang. Sedangkan tingkat akurasi yang terkecil yaitu 19.28 %, berarti menandakan dokumen tersebut termasuk plagiat tingkat sedang. Selain itu, berdasarkan analisis proses pendeteksian tingkat plagiarisme menggunakan algoritma raibin-karp dengan metode rolling hash bisa membaca karakter berupa huruf, simbol seperti titik (.), koma (,), dan lain - lain.

- Dalam penelitian Pavel Stefanovic (2019) dengan judul _The N-Grams Based Text Similarity Detection Approach Using Self-Organizing Maps and Similarity Measures_, dengan pendekatan berdasarkan teks yang dipecah menjadi n-gram dan mengevaluasinya menggunakan SOM dan similarity measure. Deteksi teks serupa dilakukan dalam tiga langkah: (1) konversi kumpulan data teks ke numerik ekspresi menggunakan n-gram; (2) perhitungan ukuran kesamaan; (3) visualisasi dataset teks menggunakan SOM dan representasi kesamaan di atasnya. Pada langkah pertama, fokus utamanya adalah membuat sekantong n-gram dari semua dataset. Berbagai jumlah kata dalam n-gram dianalisis. Selain itu, filter yang berbeda diterapkan: penghapusan angka dan tanda baca, frekuensi kata, transformasi huruf besar, stemming algoritma, dll. Analisis menunjukkan filter dan ukuran n-gram mempengaruhi hasil akhir. Untuk ini dataset, ukuran n-gram dipilih dan sama dengan tiga untuk penyelidikan eksperimental. Pada langkah kedua, empat ukuran kesamaan dihitung: cosinus, dadu, Jaccard diperpanjang, dan tumpang tindih. Hasil akhir menunjukkan bahwa persentase kemiripan tertinggi diperoleh dengan menggunakan overlap Pengukuran. Tiga nilai ukuran lainnya selalu sama dan lebih kecil. Penggunaan SOM menunjukkan bahwa SOM membantu untuk melihat hasil ringkasan kesamaan semua teks dalam bentuk visual dengan cepat. Dia sangat mudah untuk memahami teks mana yang mirip satu sama lain atau tidak. Dalam kasus kumpulan data yang dianalisis, SOM membantu mendeteksi kesamaan, dan cluster yang terbentuk dikorelasikan dengan kategoris yang diberikan deskripsi kumpulan data.

- Dalam penelitian Uswatun Hasanah, dkk (2019) dengan judul _Perbandingan Metode Cosine Similarity dan Jaccard Similarity Untuk Penilaian Otomatis Jawaban Pendek_, dinilai belum mampu memberikan jawaban yang memuaskan i dikarenakan kedua metode hanya menilai kemiripan berdasarkan susunan leksikalnya. Sementara itu, jawaban mahasiswa juga sangat bervariasi dan menggunakan kata-kata yang jauh berbeda dari jawaban kunci, walaupun pada dasarnya memiliki makna semantik yang sama. Oleh karena itu, pada penelitian selanjutnya diperlukan metode lain yang mampu menangani makna semantik pada jawaban. Bagaimanapun, metode Cosine Similarity dan Jaccard Similarity masih dapat dipertimbangkan untuk menilai jawaban pendek secara otomatis, dengan batasan bahwa pertanyaan yang digunakan mengharuskan jawaban dalam format keyword sehingga tidak memunculkan kata-kata lain yang mampu menurunkan nilai kemiripan.

## 2.2 Landasan Teori

- Sistem Infromasi
  Sistem Informasi terdiri dari dua kata yaitu Sistem dan Informasi. Sistem adalah diagram aktivitas atau activity diagram menggambarkan workflow (aliran kerja) atau aktivitas dari sebuah sistem atau proses bisnis atau menu yang ada pada perangkat lunak (Sukanto dan M.Salahuddin, 2015). Sedangkan informasi adalah sekumpulan data atau fakta yang diorganisasi atau diolah dengan cara tertentu sehingga mempunyai arti bagi penerima. (Anggerani dan Irvani, 2017). Jadi Sistem Informasi adalah sebuah aktivitas antara manusia dan teknologi yang memanajemen sebuah sistem yang mempermudah kegiatan manusia.

  Dengan adanya sebuah Sistem Informasi yang semakin berkembang saat ini, maka akan mempermudah kehidupan manusia dalam mengelola sebuah data bahkan meningkatkan produktivitas serta meminimalisir terjadinya banyak kesalahan yang terjadi. Sebagai contoh pembelajaran E-Learning dimana dengan adanya sebuah sistem informasi ini dapat mempermudah orang untuk memperoleh ilmu dari mana saja dan kapan saja.

- Hypertext Transfer Protocol Secure (HTTPS)
  Hypertext Transfer Protocol Secure (HTTPS) adalah sebuah protocol komunikasi dalam suatu jaringan internet dengan keamanan yang lebih terjamin. Disebut lebih aman karena suatu perintah atau data yang dikirim melalui HTTPS ini dilindungi dengan sistem enkripsi sehingga menyulitkan hacker untuk membobol atau mencurinya (Fakhri Aziz Firmansyah, 2019). HTTPS merupakan tingkatan dari HTTP dimana yang membedakan di HTTPS terdapat (Secure Socket Layer) SSL dan (Transport Layer Security) TSL yang digunakan untuk mengamankan data yang disimpan atau yang akan dikirim. Menurut SSL Labs pada April 2018, 33,2% dari 1.000.000 situs web teratas Alexa menggunakan HTTPS sebagai default, 57,1% dari 137.971 situs web paling populer di Internet memiliki implementasi HTTPS yang aman, dan 70% dari pemuatan halaman (diukur oleh Firefox Telemetry) menggunakan HTTPS. Jadi saat ini website sekarang sudah mulai beralih dari sebelumnya HTTP ke HTTPS karena di HTTPS lebih aman daripada HTTP yang sudah lama.

- Javascript
  Javascript adalah sebuah bahasa pemrograman tingkat tinggi yang dinamis, scripting, untyped, dan interpreter. Javascript sendiri dibuat oleh Brendan Eich dari perusahaan Nestcape pada tahun 1994 yang diberi nama Mocha pada saat itu, kemudian berganti menjadi Livescript. Karena saat itu browser yang populer adalah Nestcape, Microsoft berusaha untuk mengalahkan popularitas browser tersebut dengan Internet Explorer dan melakukan Reverse Enginering terhadap Livescript dan terciptalah JScript pada tahun 1996. Karena terdapat dua browser yang besar yang berbeda, maka dibuatlah satu standar agar mempermudah pembuatan website saat itu dan dibuatlah ECMAScript. Menurut Douglas Rockford, "JavaScript, JScript, and ECMAScript 3 Silly Name for 1 Silly Language" yang berarti bahwa ketiga nama tersebut adalah bahasa yang sama yaitu Javascript.

  a. Karakteristik Javascript

  - File
    Untuk Ekstensi dari file Javascript menggunakan ekstensi \*.js. Contoh namaFile.js.
    Setiap akhir dari kode javascript dapat menggunakan ; ataupun tidak. Sedangkan block scope di Javascript menggunakan { }.

  - Variabel
    Javascript merupakan salah satu bahasa pemrogram yang untyped / dynamicly typed yang berarti tidak mendefiniskan terlebih dahulu type variabel yang akan didefinisikan. Untuk penamaan variabel, terdapat beberapa keyword yaitu var, let, dan const. Untuk var, dan let, nilai variabel dapat berubah atau diisi ulang, sedangkan const nilai variabelnya tidak dapat diubah. Perbedaan var dan let sendiri terletak pada hoistingnya. Sedangkan untuk penamaan variabel, hampir sama dengan beebrapa bahasa pemrograman lainnya seperti karakter pertama variabel tidak boleh angka, menggunakan penulisan camelCase, dan untuk keyword const yang merupakan variabel const biasanya menggunakan snake_case dan semuanya huruf kapital. Contoh :
    ```Javascript
    var value = 10 // Contoh Penggunaan var
    let nilai = 'Delapan' // Contoh Penggunaan let
    const SPEED_OF_LIGHT = 3.14 // Contoh Penggunaan const
    ```
  - Tipe Data
    Javascript memiliki beberapa tipe data seperti String, Number atau Integer, Boolean, Array, Object, dan Undifined. Untuk mengetahui tipe data dari sebuah variabel dapat menggunakan keyword typeof. Contoh :
    ```Javascript
    let name = 'Aris Akhyar Abdillah' // String
    let age = 22 // Number atau Integer
    let male = true // Boolean
    let family = ['Father', 'Mother', 'Son', 'Girl'] // Array
    let cv = {
      fullName : 'Aris Akhyar Addillah',
      nim : 'H071171505'
    } // Object
    let girlfreind = undefined // Undefined
    ```
  - Synchronous dan Asynchronous
    Secara sederhana, Syncronus dan Asynchronous merupakan tahapan dalam mengeksekusi sebuah kode dimana Synchronous mengeksekusi sebuah kode perbaris sesuai urutan kode yang dituliskan. Sedangkan Asynchronous, tidak selalu seperti Synchronous, tapi melihat waktu proses dari kode tersebut. Penggunaan Asynchronous tidak akan menunggu suatu kode selesai dijalankan, tetapi berlanjut ke kode selanjutnya. Contoh :

    ```Javascript
    // Menggunakan Synchronous

    console.log('What Is Your Name ?')
    console.log('Hello World')
    console.log('My Name is Aris')

    // Output :
    // What Is Your Name ?
    // Hello World
    // My Name is Aris

    // Menggunakan Asynchronous

    setTimeout(function() {
      console.log('What Is Your Name ?')
    }, 1500)
    console.log('Hello World')
    setTimeout(function() {
      console.log('My Name is Aris')
    }, 1000)

    // Output :
    // Hello World
    // My Name is Aris
    // What Is Your Name ?
    ```

    Jika melihat output dari dua program diatas antara menggunakan Synchronous dan Asynchronous terdapat perbedaan urutan dari hasil output, dimana Synchronous memiliki output sesuai dari urutan baris kode sedangkan Asynchronous berbeda dimana output yang dihasilkan berdasarkan jumlah waktu pengeksekusian dari kode tersebut yang disimulasikan menggunakan setTimeout() dari pengeksekusian paling cepat hingga yang paling lambat.

  b. NodeJS
  Node.js adalah runtime environment untuk JavaScript yang bersifat open-source dan cross-platform. Dengan Node.js kita dapat menjalankan kode JavaScript di mana pun, tidak hanya terbatas pada lingkungan browser. Seperti diketahui bahawa Javascript hanya dapat berjalan pada sebuah web browser, kemudian Ryan Dahl, membuat sebuah runtime environment dengan mengeluarkan engine Javasscript dari Chrome yaitu V8 Javascript Engine menggunakan bahaasa C agar Javascript dapat dijalankan diluar browser. Akhirnya tercipta NodeJS pada tahun 2009. Dengan Begitu, Javascript yang sebelumnya hanya bisa di client side dengan adanya NodeJS bisa juga di server side. Beberapa fitur yang terdapat di NodeJS seperti Asynchronous & Event-driven, Single Threaded but Highly Scalable.

  c. Express JS
  Menurut Website resmi dari Express JS adalah 'Fast, unopinionated, minimalist web framework for Nodejs'. Express JS sendiri merupakan salah satu web framework khusus untuk NodeJS dimana kita dapat membuat sebuah website yang cepat, sederhana, dengan struktur yang tidak ditentukan atau tergantung dari pengguna Express JS sendiri.

- Database
  Database atau basis data adalah kumpulan informasi yang disimpan di dalam komputer secara sistematik sehingga dapat diperiksa menggunakan suatu program komputer untuk memperoleh informasi dari basis data tersebut (Andry Andaru). Berdasarkan definisi database, database berfungsi untuk menyimpan catatan atau sebuah data pada sebuah penyimpanan yang kemudian akan digunakan pada waktu lainnya. Pada umumnya, database sudah pasti memiliki key dan value, walaupun istilah ini berbeda ditiap tiap jenis database yang ada. Adapun beberapa jenis database seperti Operational Database, Database Warehouse, Distributed Database, Relational Database, dan End User Database.

  a. SQL dan NoSQL
  SQL dan NoSQL merupakan salah satu contoh dari Relational Database yang populer saat ini. SQL (Structured Query Language) merupakan bahasa yang digunakan untuk mengelola data secara relational. SQL sendiri memiliki ciri yaitu memiliki tabel yang terdiri dengan row atau record dan field yang bisa memiliki relasi dengan tabel lainnya. Untuk tiap data yang ada didalam tabel, harus memiliki skema yang sama untuk tiap recordnya. Contoh dari SQL seperti MySQL, PostgreSQL, dan MariaDB. Berbeda dengan NoSQL (Not Only Structured Query Language) yang merupakan bahasa untuk mengelola data secara Non Relational. Berbeda dengan SQL yang menggunakan tabel untuk menyimpan data. NoSQL memilik banyak jenis tempat untuk menyimpan data seperti Document Database, Key-Value Database, dan Graph Database. NoSQL juga tidak memiliki skema sehingga untuk menyimpan data bisa secara flexibel. Contoh dari NoSQL seperti MongoDB, Redis, Neo4j, dan Cassandra.

  b. MongoDB
  MongoDB merupakan salah satu contoh dari NoSQL yang dikembangkan menggunakan bahasa pemrograman C++ yang rilis pertama kali pada tanggal 11 Februari 2009. MongoDB adalah salah satu contoh Document Database yang dimana tiap - tiap datanya merupakan sebuah JSON (Javascript Object Notation) atau dalam MongoDB disebut BSON (Binary JSON). Hingga saat ini, MongoDB sudah digunakan lebih dari 85 Juta pengguna diseluruh dunia dan sudah banyak perusahaan besar yang menggunakan database ini seperti EBay, Google, Adobe, dan EA. Salah satu contoh data yang terdapat di MongoDB :

  ```Javascript
  {
    _id : '91829jw1jooojo2',
    firstName : 'Aris',
    lastName : 'Akhyar',
    age : 20
    hobbies : ['eat', 'drink']
  }
  ```

- Jurnal
  Jurnal merupakan bagian dari jenis terbitan berseri yang ada diperpustakaan, adapun pengertian jurnal menurut High Beam “Journal is the collection and periodic publication or transmission of news and the result of research through media”, artinya bahwa jurnal merupakan suatu koleksi dan terbitan berkala atau transmisi mengenai berita dan hasil-hasil penelitian mengenai media. Jurnal sendiri terbagi atas dua format yaitu tercetak dan digital (e-journal). Untuk format digital jurnal dikemas dalam dua format , yaitu bentuk CD-ROM dan dalam bentuk akses secara online melalui internet. E-Journal dipahami sebagai publikasi ilmiah dalam format elektronik dan mempunyai ISSN (International Standard Serial Number) yang format dokumennya biasanya PDF (Rusydi 2014).

  Penggunaan kata jurnal untuk berbagai bidang juga memberi arti yang bervariasi, misalnya jurnal dalam bidang ekonomi menunjukan sistem pembukuan rangkap. Jurnal dalam bidang pelayaran diartikan sebagai logbook berarti buku untuk mencatat semua kejadian selama pelayaran. Jurnal sebenarnya merupakan publikasi ilmiah yang memuat informasi tentang hasil kegiatan dalam bidang ilmu pengetahuan dan teknologi minimal harus mencakup kumpulan atau kumulasi pengetahuan baru, pengamatan empiris dan pengembangan gagasan atau usulan. Dengan demikian jurnal merupakan representasi dari pengetahuan baru tentang perkembangan ilmu pengetahuan yang dilaksanakan secara empriris dan biasanya merupakan gagasan yang terbaru.

- Plagiarisme
  Plagiarisme berasal dari bahasa Latin “plagiare” yang berarti mencuri. Plagiarisme berasal dari kata plagiat yang berarti pengambilan karangan (pendapat dan sebagainya) orang lain dan menjadikannya seolah-olah karangan (pendapat dan sebagainya) sendiri, misalnya menerbitkan karya tulis orang lain atas nama dirinya sendiri. Sehingga dapat diartikan plagiarisme merupakan tindakan mencuri gagasan hasil penelitian orang lain, untuk kemudian disajikan seolah-olah milik sendiri (Ridhatillah, 2013). Tindakan plagiarisme merupakan salah satu tindakan yang melanggar hak cipta. Hak Cipta itu sendiri merupakan hak eksklusif untuk Pencipta ataupun penerima hak buat mengumumkan ataupun perbanyak Ciptaannya ataupun membagikan izin buat itu dengan tidak kurangi pembatasan- pembatasan bagi peraturan perundang- undangan yang berlaku. Jika terjadi pelanggaran tersebut, dapat dikenai pelanggaran hak cipta dPasal 72 ayat UUHC dengan dipidana dengan pidana penjara pendek selama 1 bulan serta/ ataupun denda sangat sedikitnya Rp1.000.000,00, ataupun pidana penjara lama 7 tahun serta/ ataupun denda sangat sebanyak Rp5.000.000.000,00.

- Dice Similarity
  Dice Similarity atau Sørensen–Dice coefficient merupakan salah satu algoritma yang mengukur kesamaan antara dua set data. Algoritma ini banyak digunakan dalam validasi algoritma segmentasi gambar yang dibuat dengan AI, tetapi ini adalah konsep yang jauh lebih umum yang dapat diterapkan pada kumpulan data untuk berbagai aplikasi termasuk NLP.
- Jaccard Similarity
