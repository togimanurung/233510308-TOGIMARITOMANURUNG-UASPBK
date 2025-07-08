<template>
  <div>
    <h1>Daftar Produk</h1>
    <div class="product-list">
      <ProductCard
        v-for="product in products"
        :key="product.id"
        :product="product"
      />
    </div>
  </div>
</template>

<script>
import ProductCard from '../components/ProductCard.vue';

export default {
  components: { ProductCard },
  data() {
    return {
      products: [
        {
          id: 1,
          name: "Beras Kencur",
          description: "Minuman tradisional menyegarkan",
          price: 10000,
          image: "beras-kencur.jpg"
        },
        {
          id: 2,
          name: "Temulawak",
          description: "Meningkatkan nafsu makan dan kekebalan tubuh",
          price: 12000,
          image: "temulawak.jpg"
        },
        {
          id: 3,
          name: "Cabe Puyang",
          description: "Meredakan pegal dan masuk angin",
          price: 11000,
          image: "cabe-puyang.jpg"
        },
        {
          id: 4,
          name: "Daun Sirih",
          description: "Mengatasi bau badan dan keputihan",
          price: 9500,
          image: "daun-sirih.jpg"
        },
        {
          id: 5,
          name: "Kunyit Asam",
          description: "Mengurangi nyeri haid dan menyegarkan tubuh",
          price: 11500,
          image: "Kunyit-Asam.jpg"
        }
      ]
    };
  }
};
</script>

<style scoped>
.product-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
}
</style>
