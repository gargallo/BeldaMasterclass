<template>
  <div>
    products
    <ul>
      <li v-for="product in products" :key="product.id">
        <img :src="product.image" :alt="product.title">
        <h2>{{ product.title }}</h2>
        <p>{{ product.price }}</p>
        <button>Ver Detalle</button>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'ProductGrid',
  props: {
    products: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style scoped>

ul {
  @apply grid grid-cols-1 lg:grid-cols-4 gap-16
}
li {
  @apply flex flex-col h-full justify-end
}
h2, p {
  @apply text-center
}
img {
  @apply m-auto py-8
}
</style>
