Toko Jamu Nusantara
Toko Jamu Nusantara adalah sebuah website e-commerce sederhana berbasis Vue 3 dan Vite yang dirancang untuk menjual berbagai produk jamu dan obat tradisional khas Indonesia. Aplikasi ini dilengkapi dengan fitur login, daftar produk, keranjang belanja, dan halaman checkout, serta desain modern yang responsif dan menarik.

Fitur Utama
Halaman Login

Pengguna wajib login terlebih dahulu sebelum mengakses website.
Validasi login menggunakan username dan password (statis) yang disimpan di sisi klien menggunakan localStorage.
Halaman Beranda

Menampilkan sambutan kepada pengguna.
Latar belakang menggunakan gambar herbal khas Indonesia.
Tombol navigasi ke halaman produk.
Halaman Produk

Menampilkan daftar produk jamu lengkap dengan:

Gambar produk.
Nama produk.
Deskripsi produk.
Harga produk.
Setiap produk dapat ditambahkan ke dalam keranjang.

Halaman Keranjang

Menampilkan semua produk yang ditambahkan.
Menampilkan total harga dan tombol untuk menghapus produk dari keranjang.
Menampilkan gambar dari setiap produk yang dibeli.
Halaman Checkout

Menampilkan kembali daftar produk yang akan dibeli.
Informasi lengkap seperti gambar, nama produk, jumlah, dan harga.
Tombol konfirmasi pembelian.
Fitur Logout

Menghapus status login dari localStorage.
Setelah logout, pengguna akan diarahkan kembali ke halaman login.
Desain Responsif

Desain menggunakan kombinasi layout grid dan flexbox.
Menggunakan latar transparan pada konten utama dengan gambar latar yang menyatu.
Navigasi menggunakan Vue Router dan komponen Navbar.
Teknologi yang Digunakan
Vue 3
Vite
Pinia (state management)
Vue Router
LocalStorage (penyimpanan status login)
HTML5 dan CSS3
Struktur Folder
UASPBK/
├── public/
│   └── images/
│       ├── logo-jamu.jpg
│       ├── bg-home.jpg
│       ├── beras-kencur.jpg
│       ├── temulawak.jpg
│       ├── cabe-puyang.jpg
│       ├── daun-sirih.jpg
│       └── Kunyit-Asam.jpg
├── src/
│   ├── assets/
│   ├── components/
│   │   ├── Navbar.vue
│   │   ├── ProductCard.vue
│   ├── pages/
│   │   ├── HomePage.vue
│   │   ├── LoginPage.vue
│   │   ├── ProductPage.vue
│   │   ├── CartPage.vue
│   │   └── CheckoutPage.vue
│   ├── store/
│   │   ├── auth.js
│   │   └── cart.js
│   ├── App.vue
│   └── main.js
├── vite.config.js
└── package.json
Cara Menjalankan Project
Clone repository ini:

git clone https://github.com/username/uaspbk.git
cd uaspbk
Install semua dependency:

npm install
Jalankan server pengembangan:

npm run dev
Akses melalui browser:

http://localhost:5173
Informasi Login
Username: admin Password: admin

Catatan
Semua gambar dimasukkan ke dalam folder public/images untuk dapat diakses langsung dari HTML.
Karena ini adalah aplikasi statis, data produk tidak terhubung dengan database dan hanya bersifat simulasi.
Sistem login sederhana hanya menggunakan validasi di sisi klien dan tidak cocok untuk aplikasi produksi.
Tujuan Proyek
Website ini dikembangkan sebagai bagian dari tugas akhir mata kuliah Pengembangan Berbasis Komponen (PBK), dengan tujuan menerapkan konsep-komponen Vue, routing, state management, serta interaksi pengguna melalui form dan navigasi.
