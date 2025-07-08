<template>
  <div class="card">
    <img :src="`/images/${product.image}`" :alt="product.name" class="product-image" />
    <div class="info">
      <h3>{{ product.name }}</h3>
      <p class="desc">{{ product.description }}</p>
      <p class="price">Rp {{ product.price.toLocaleString('id-ID') }}</p>
      <button @click="addToCart">+ Tambah ke Keranjang</button>
    </div>
  </div>
</template>

<script>
import { useCartStore } from '../store/cartStore';

export default {
  props: {
    product: Object
  },
  setup(props) {
    const cart = useCartStore();
    const addToCart = () => {
      cart.addToCart(props.product);
    };
    return { addToCart };
  }
};
</script>

<style scoped>
.card {
  background-color: rgb(209, 195, 195);
  border-radius: 16px;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.08);
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: transform 0.3s ease;
}
.card:hover {
  transform: scale(1.02);
}
.product-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}
.info {
  padding: 1rem;
  text-align: center;
}
.desc {
  font-size: 0.9rem;
  color: #555;
}
.price {
  font-weight: bold;
  margin: 0.5rem 0;
}
button {
  background-color: #5d3a00;
  color: rgb(255, 254, 254);
  border: none;
  padding: 0.5rem 1rem;
  border-radius: 8px;
  cursor: pointer;
  margin-top: 0.5rem;
}
button:hover {
  background-color: #7a4e00;
}
</style>
