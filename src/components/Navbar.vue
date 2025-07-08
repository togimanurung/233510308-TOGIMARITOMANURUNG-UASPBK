<template>
  <nav>
    <router-link to="/beranda">Beranda</router-link>
    <router-link to="/produk">Produk</router-link>
    <router-link to="/keranjang">Keranjang</router-link>
    <router-link to="/checkout">Checkout</router-link>
    <button v-if="isLoggedIn" @click="logout">Logout</button>
    <router-link v-else to="/login">Login</router-link>
  </nav>
</template>

<script>
import { ref, onMounted } from 'vue';
import { useRouter } from 'vue-router';

export default {
  setup() {
    const router = useRouter();
    const isLoggedIn = ref(false);

    onMounted(() => {
      // Ambil status login dari localStorage saat komponen dimuat
      isLoggedIn.value = localStorage.getItem('isLoggedIn') === 'true';
    });

    const logout = () => {
      localStorage.removeItem('isLoggedIn');
      isLoggedIn.value = false;
      router.push('/login');
    };

    return { isLoggedIn, logout };
  }
};
</script>

<style scoped>
nav {
  display: flex;
  gap: 1rem;
  padding: 1rem;
  background-color: #ec8116;
  color: white;
  justify-content: flex-end;
}
a {
  color: white;
  text-decoration: none;
}
button {
  background-color: red;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 6px;
  cursor: pointer;
}
</style>
