
## Toko Jamu Nusantara

**Toko Jamu Nusantara** adalah sebuah aplikasi web e-commerce berbasis **Vue 3 dan Vite** yang dirancang untuk menjual berbagai produk jamu dan obat tradisional khas Indonesia. Aplikasi ini bertujuan untuk membantu pelestarian warisan budaya melalui transformasi digital dengan menyediakan platform modern yang mudah digunakan oleh pengguna.

Aplikasi ini dikembangkan sebagai bagian dari **Tugas Akhir Mata Kuliah Pengembangan Berbasis Komponen (PBK)** dan digunakan sebagai studi kasus penerapan konsep Vue.js seperti komponen, routing, state management, serta interaksi pengguna melalui formulir dan navigasi.

---

## Tujuan Proyek

1. Membangun aplikasi e-commerce berbasis web untuk menjual jamu tradisional khas Indonesia.
2. Menyediakan fitur-fitur utama seperti:

   * Login dan logout pengguna
   * Daftar produk jamu
   * Keranjang belanja
   * Proses checkout
3. Menggunakan teknologi modern seperti Vue 3, Vite, Pinia, dan Vue Router.
4. Menyajikan desain yang responsif, sederhana, dan menarik dengan sentuhan lokal.

---

## Fitur Utama

### Halaman Login

* Halaman login ditampilkan pertama kali ketika aplikasi diakses.
* Validasi dilakukan terhadap username dan password (admin/admin) yang disimpan di `localStorage`.
* Setelah berhasil login, pengguna diarahkan ke halaman beranda.
* Jika login gagal, pengguna tetap berada di halaman login.

### Halaman Beranda (HomePage.vue)

* Menampilkan sambutan kepada pengguna dan deskripsi singkat mengenai toko.
* Menggunakan gambar latar bertema herbal atau jamu tradisional dari file `bg-home.jpg`.
* Dilengkapi dengan tombol navigasi ke halaman daftar produk.
* Tampilan antarmuka menggunakan layout fleksibel dan transparansi latar.

### Halaman Produk (ProductList.vue)

* Menampilkan daftar produk jamu yang diambil dari API `json-server`.
* Setiap produk mencakup:

  * Gambar produk
  * Nama produk
  * Deskripsi singkat
  * Harga produk
  * Tombol "Tambah ke Keranjang"
* Tampilan produk disusun menggunakan layout grid yang responsif.

### Halaman Keranjang (CartPage.vue)

* Menampilkan semua produk yang telah ditambahkan oleh pengguna.
* Informasi produk yang ditampilkan meliputi:

  * Nama dan gambar produk
  * Jumlah yang dibeli
  * Harga total per item
* Tersedia tombol untuk menambah atau mengurangi jumlah produk dan menghapus produk dari keranjang.
* Menampilkan total keseluruhan harga belanja.
* Terdapat tombol untuk melanjutkan ke halaman checkout.

### Halaman Checkout (CheckoutPage.vue)

* Menampilkan ringkasan pembelian secara menyeluruh:

  * Gambar produk
  * Nama, jumlah, dan harga
* Dilengkapi dengan tombol untuk mengonfirmasi pembelian.
* Setelah konfirmasi, keranjang akan dikosongkan dan pengguna diarahkan kembali ke halaman utama.

### Navigasi (Navbar.vue)

* Terdapat tautan ke halaman:

  * Beranda
  * Produk
  * Keranjang
  * Checkout
  * Login/Logout
* Jika pengguna sudah login, tombol "Logout" akan muncul.
* Navigasi menggunakan Vue Router untuk berpindah antar halaman.

---

## Teknologi yang Digunakan

* **Framework:** Vue.js 3 + Vite
* **State Management:** Pinia
* **Routing:** Vue Router
* **Styling:** CSS3 (Flexbox dan Grid Layout)
* **Assets:** Gambar produk dan latar disimpan di folder `public/images`

---

## Struktur Folder

```
uaspbk/
├── public/
│   └── images/
│       ├── bg-home.jpg
│       ├── beras-kencur.jpg
│       ├── temulawak.jpg
│       ├── cabe-puyang.jpg
│       ├── daun-sirih.jpg
│       └── kunyit-asam.jpg
├── src/
│   ├── components/
│   │   ├── Navbar.vue
│   │   └── ProductCard.vue
│   ├── pages/
│   │   ├── HomePage.vue
│   │   ├── LoginPage.vue
│   │   ├── ProductList.vue
│   │   ├── CartPage.vue
│   │   └── CheckoutPage.vue
│   ├── store/
│   │   ├── auth.js
│   │   └── cart.js
│   ├── App.vue
│   └── main.js
├── db.json
├── package.json
└── vite.config.js
```

---


## Informasi Login

* **Username:** admin
* **Password:** admin

---

