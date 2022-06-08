<template>
  <div>
    <h1>Shop</h1>
    <products-grid :products="products" />
  </div>
</template>
<script>
export default {
  name: 'ProductListing',
  async asyncData ({ $axios }) {
    const products = await $axios.$get('https://fakestoreapi.com/products')
    return { products }
  }
}
</script>
