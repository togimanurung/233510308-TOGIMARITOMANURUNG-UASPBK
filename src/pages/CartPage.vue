<template>
  <div>
    <h1>Keranjang Belanja</h1>
    <div v-if="cart.items.length === 0">
      <p>Keranjang kosong</p>
    </div>
    <div v-else class="cart-list">
      <div
        v-for="item in cart.items"
        :key="item.id"
        class="cart-item"
      >
        <img :src="`/images/${item.image}`" :alt="item.name" class="product-image" />
        <div class="item-info">
          <h3>{{ item.name }}</h3>
          <p>{{ item.description }}</p>
          <p>Rp {{ item.price.toLocaleString('id-ID') }} x {{ item.quantity }}</p>
          <div class="quantity-controls">
            <button @click="cart.decrement(item.id)">-</button>
            <span>{{ item.quantity }}</span>
            <button @click="cart.increment(item.id)">+</button>
            <button @click="cart.removeFromCart(item.id)" class="delete">Hapus</button>
          </div>
        </div>
      </div>

      <hr />
      <p><strong>Total: Rp {{ cart.totalPrice.toLocaleString('id-ID') }}</strong></p>
      <router-link to="/checkout">
        <button class="checkout-button">Checkout</button>
      </router-link>
    </div>
  </div>
</template>

<script>
import { useCartStore } from '../store/cartStore';

export default {
  setup() {
    const cart = useCartStore();
    return { cart };
  }
};
</script>

<style scoped>
.cart-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-top: 1rem;
}

.cart-item {
  display: flex;
  background: #a69d9d;
  border: 1px solid #7c7171;
  border-radius: 12px;
  padding: 1rem;
  gap: 1rem;
  align-items: center;
}

.product-image {
  width: 100px;
  height: 100px;
  object-fit: cover;
  border-radius: 8px;
  flex-shrink: 0;
}

.item-info {
  flex-grow: 1;
}

.quantity-controls {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  margin-top: 0.5rem;
}

.quantity-controls button {
  background-color: #5d3a00;
  color: white;
  border: none;
  padding: 4px 10px;
  border-radius: 6px;
  cursor: pointer;
}

.quantity-controls .delete {
  background-color: red;
}

.checkout-button {
  background-color: #fa900f;
  color: rgb(255, 251, 251);
  padding: 0.75rem 1.5rem;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  margin-top: 1rem;
}
</style>
