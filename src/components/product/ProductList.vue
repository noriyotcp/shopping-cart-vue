<template>
  <div>
    <product-list-item />
    <product-list-item />
    <product-list-item />
  </div>
</template>

<script>
import ProductListItem from './ProductListItem'
export default {
  name: 'ProductList',
  components: {
    ProductListItem
  }
};
</script>
