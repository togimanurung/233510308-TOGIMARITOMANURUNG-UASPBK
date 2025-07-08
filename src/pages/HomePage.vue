<template>
  <div class="home-container">
    <img src="/images/logo-jamu.jpg" alt="Logo Jamu" class="logo" />
    <h1>
      <span>Selamat Datang di</span><br /><strong>Toko Jamu <span class="highlight">Nusantara</span></strong>
    </h1>
    <p>
      Jamu dan obat tradisional Indonesia untuk kesehatan alami.
    </p>
    <router-link to="/produk" class="btn">Lihat Produk</router-link>
  </div>
</template>

<style scoped>
.home-container {
  text-align: center;
  padding: 40px 15px;
  background: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url('/images/bg-home.jpg') no-repeat center center;
  background-size: cover;
  border-radius: 12px;
  max-width: 600px;
  margin: 40px auto;
  color: #fff;
  min-height: 60vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 0 3px 8px rgba(0, 0, 0, 0.2);
}

.logo {
  width: 90px;
  margin-bottom: 1rem;
  border-radius: 8px;
}

h1 {
  font-size: 2rem;
  line-height: 1.3;
}

.highlight {
  color: #ffcc00;
}

p {
  margin-top: 1rem;
  font-size: 1rem;
}

.btn {
  margin-top: 1.5rem;
  display: inline-block;
  padding: 0.6rem 1.2rem;
  background-color: #ffc107;
  color: #000;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  transition: background-color 0.3s ease;
}

.btn:hover {
  background-color: #ff9900;
}
</style>
