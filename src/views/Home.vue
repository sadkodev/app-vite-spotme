<template>
  <div>
    <article v-for="product in products">
      <h1>{{ product.title }}</h1>
      <p>{{ product.description }}</p>
      <p>price : {{ product.price }}</p>
    </article>
  </div>
</template>

<script>
import { useProductStore } from '../stores/ProductsStore'

export default {
  name: 'Home',
  data: () => {
    return { products: useProductStore().products }
  },
}
</script>
<style scoped></style>
