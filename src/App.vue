<template>
  <div id="app">
    <HeaderComp></HeaderComp>
    <p> добавили на удаленном репозитории </p>

    <ol>
      <ul v-for="product in products" :key="product.id">
        <ProductDetails :product="product"></ProductDetails>
      </ul>
    </ol>

<FooterComp></FooterComp>

  </div>
</template>

<script>
import ProductDetails from './components/ProductDetails.vue';
import HeaderComp from './components/HeaderComp.vue';
import FooterComp from './components/FooterComp.vue';

export default {
  name: 'App',
  components: {
    ProductDetails,
    HeaderComp,
    FooterComp
},
  data() {
    return {
      products: [
        { name: 'Рубашка', price: 50, available: true },
        { name: 'Галстук', price: 10, available: true },
        { name: 'Джинсы', price: 70, available: false },
        { name: 'Ботинки', price: 100, available: false },
        { name: 'Пиджак', price: 30, available: true },
      ]
    };
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
