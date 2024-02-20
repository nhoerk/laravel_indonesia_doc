Dokumentasi Laravel dalam bahasa Indonesia

# Berkenalan dengan Laravel

Laravel adalah sebuah kerangka kerja aplikasi web dengan sintaks yang ekspresif dan elegan. Sebuah kerangka kerja web menyediakan struktur dan titik awal untuk membuat aplikasi Anda, memungkinkan Anda fokus pada menciptakan sesuatu yang menakjubkan sementara kami mengurus detailnya.

Laravel berusaha memberikan pengalaman pengembang yang luar biasa sambil menyediakan fitur-fitur yang kuat seperti dependency injection yang komprehensif, lapisan abstraksi basis data yang ekspresif, antrean dan pekerjaan yang terjadwal, pengujian unit dan integrasi, dan lainnya.

Baik Anda baru mengenal kerangka kerja aplikasi web PHP atau memiliki pengalaman bertahun-tahun, Laravel adalah kerangka kerja yang dapat tumbuh bersama Anda. Kami akan membantu Anda melangkah pertama sebagai pengembang web atau memberikan dorongan saat Anda meningkatkan keahlian Anda ke tingkat berikutnya. Kami tak sabar untuk melihat apa yang Anda bangun.

Baru mengenal Laravel? Cek [Bootcamp Laravel](https://bootcamp.laravel.com/) untuk tur langsung kerangka kerja sambil kami membimbing Anda dalam membangun aplikasi Laravel pertama Anda.

# Mengapa Laravel?
Terdapat berbagai alat dan kerangka kerja yang tersedia untuk Anda saat membangun aplikasi web. Namun, kami percaya bahwa Laravel adalah pilihan terbaik untuk membangun aplikasi web modern dan full-stack.

### Sebuah Kerangka Kerja Progresif
Kami suka menyebut Laravel sebagai kerangka kerja "progresif". Dengan itu, kami maksudkan bahwa Laravel tumbuh bersama Anda. Jika Anda baru mengambil langkah pertama dalam pengembangan web, perpustakaan dokumentasi, panduan, dan tutorial video yang luas dari Laravel akan membantu Anda belajar tanpa menjadi terlalu kewalahan.

Jika Anda seorang pengembang senior, Laravel memberikan Anda alat-alat yang kokoh untuk dependency injection, pengujian unit, antrean, peristiwa real-time, dan lainnya. Laravel disesuaikan dengan baik untuk membangun aplikasi web profesional dan siap untuk menangani beban kerja perusahaan.

### Sebuah Kerangka Kerja yang Dapat Diskalakan
Laravel sangat dapat diskalakan. Berkat sifat yang ramah terhadap skalabilitas dari PHP dan dukungan bawaan Laravel untuk sistem cache terdistribusi yang cepat seperti Redis, melakukan skalabilitas horizontal dengan Laravel menjadi mudah. Bahkan, aplikasi Laravel telah dengan mudah diskalakan untuk menangani ratusan juta permintaan per bulan.

Butuh skalabilitas ekstrem? Platform seperti [Laravel Vapor](https://vapor.laravel.com/) memungkinkan Anda menjalankan aplikasi Laravel Anda dengan skala yang hampir tak terbatas pada teknologi serverless terbaru AWS.

### Sebuah Kerangka Kerja Komunitas
Laravel menggabungkan paket-paket terbaik dalam ekosistem PHP untuk menawarkan kerangka kerja yang paling kokoh dan ramah pengembang yang tersedia. Selain itu, ribuan pengembang berbakat dari seluruh dunia telah berkontribusi pada kerangka kerja tersebut. Siapa tahu, mungkin Anda juga akan menjadi kontributor Laravel.

# Membuat Proyek Laravel
Sebelum membuat proyek Laravel pertama Anda, pastikan mesin lokal Anda telah memiliki PHP dan Composer terinstal. Jika Anda mengembangkan di macOS, PHP dan Composer dapat diinstal dalam hitungan menit melalui Laravel Herd. Selain itu, kami sarankan untuk menginstal Node dan NPM.

Setelah Anda menginstal PHP dan Composer, Anda dapat membuat proyek Laravel baru melalui perintah create-project dari Composer:

```bash
composer create-project --prefer-dist laravel/laravel nama-aplikasi-contoh
```

Atau, Anda dapat membuat proyek Laravel baru dengan menginstal global installer Laravel melalui Composer:

```bash
composer global require laravel/installer

laravel new nama-aplikasi-contoh
```

Setelah proyek telah dibuat, mulailah server pengembangan lokal Laravel menggunakan perintah serve di Laravel Artisan:

```bash
cd nama-aplikasi-contoh

php artisan serve
```

Setelah Anda memulai server pengembangan Artisan, aplikasi Anda akan dapat diakses melalui browser web Anda di http://localhost:8000. Selanjutnya, Anda siap untuk melangkah ke ekosistem Laravel selanjutnya. Tentu saja, Anda juga mungkin ingin mengkonfigurasi sebuah basis data.

Jika Anda ingin mendapatkan awal yang cepat saat mengembangkan aplikasi Laravel Anda, pertimbangkan untuk menggunakan salah satu [starter kit](https://laravel.com/docs/10.x/starter-kits) kami. Starter kit Laravel menyediakan kerangka kerja otentikasi backend dan frontend untuk aplikasi Laravel baru Anda.

# Konfigurasi Awal
Semua file konfigurasi untuk kerangka kerja Laravel disimpan dalam direktori `config`. Setiap opsi didokumentasikan, jadi silakan telusuri file-file tersebut dan kenali opsi yang tersedia untuk Anda.

Laravel hampir tidak memerlukan konfigurasi tambahan secara default. Anda bebas untuk mulai mengembangkan! Namun, Anda mungkin ingin meninjau file `config/app.php` dan dokumentasinya. Ini berisi beberapa opsi seperti `timezone` dan `locale` yang mungkin ingin Anda ubah sesuai dengan aplikasi Anda.

### Konfigurasi Berbasis Lingkungan
Karena banyak nilai opsi konfigurasi Laravel dapat bervariasi tergantung pada apakah aplikasi Anda berjalan di mesin lokal atau di server web produksi, banyak nilai konfigurasi penting didefinisikan menggunakan file `.env` yang ada di root aplikasi Anda.

File `.env` Anda sebaiknya tidak dicantumkan dalam kontrol sumber aplikasi Anda, karena setiap pengembang/server yang menggunakan aplikasi Anda mungkin memerlukan konfigurasi lingkungan yang berbeda. Selain itu, ini akan menjadi risiko keamanan jika seorang intruder mendapatkan akses ke repositori kontrol sumber Anda, karena setiap kredensial sensitif akan terbuka.

Untuk informasi lebih lanjut tentang file `.env` dan konfigurasi berbasis lingkungan, Anda dapat memeriksa [dokumentasi konfigurasi](https://laravel.com/docs/10.x/configuration#environment-configuration) lengkapnya.

### Database dan Migrasi
Sekarang setelah Anda telah membuat aplikasi Laravel Anda, Anda mungkin ingin menyimpan beberapa data dalam basis data. Secara default, file konfigurasi `.env` aplikasi Anda menentukan bahwa Laravel akan berinteraksi dengan basis data MySQL dan akan mengakses basis data di `127.0.0.1`.

Jika Anda mengembangkan di macOS dan perlu menginstal MySQL, Postgres, atau Redis secara lokal, pertimbangkan untuk menggunakan [DBngin](https://dbngin.com/).
