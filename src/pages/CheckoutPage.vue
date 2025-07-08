<template>
  <div>
    <h1>Checkout</h1>
    <div v-if="cart.items.length === 0">Tidak ada produk untuk checkout</div>
    <div v-else class="checkout-list">
      <div
        v-for="item in cart.items"
        :key="item.id"
        class="checkout-item"
      >
        <img :src="`/images/${item.image}`" :alt="item.name" />
        <div>
          <h3>{{ item.name }}</h3>
          <p>{{ item.quantity }} x Rp {{ item.price.toLocaleString('id-ID') }}</p>
        </div>
      </div>
      <hr />
      <p><strong>Total Bayar: Rp {{ cart.totalPrice.toLocaleString('id-ID') }}</strong></p>
      <button @click="checkout">Konfirmasi Pembayaran</button>
    </div>
  </div>
</template>

<script>
import { useCartStore } from '../store/cartStore';
import { useRouter } from 'vue-router';

export default {
  setup() {
    const cart = useCartStore();
    const router = useRouter();
    const checkout = () => {
      alert('Pembayaran berhasil!');
      cart.clearCart();
      router.push('/');
    };
    return { cart, checkout };
  }
};
</script>

<style scoped>
.checkout-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-top: 1rem;
}
.checkout-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  background: #635a5a;
  border: 1px solid #4d4242;
  border-radius: 12px;
  padding: 1rem;
}
.checkout-item img {
  width: 80px;
  height: 80px;
  object-fit: cover;
  border-radius: 8px;
}
button {
  background-color: #f7a013;
  color: rgb(255, 243, 243);
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 8px;
  cursor: pointer;
}
button:hover {
  background-color: #ffa60c;
}
</style>
