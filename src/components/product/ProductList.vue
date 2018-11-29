<template>
  <div>
    <product-list-item v-for="product in productItems" :key="product.id" :product="product" />
  </div>
</template>

<script>
import ProductListItem from './ProductListItem'
import { mapGetters } from 'vuex'

export default {
  name: 'ProductList',
  components: {
    ProductListItem
  },
  created() {
    this.$store.dispatch('fetchProducts')
  },
  computed: {
    ...mapGetters(['productItems'])
  }
};
</script>
