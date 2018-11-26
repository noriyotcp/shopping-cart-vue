<template>
  <div>
    <div class="container">
      <div class="row">
        <div class="col-sm-7">
          <cart-list />
        </div>
        <div class="col-sm-5">
          <product-list />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ProductList from './components/product/ProductList'
import CartList from './components/cart/CartList'
export default {
    name: 'app',
    components: {
      ProductList,
      CartList
    }
};
</script>

<style >
.product-card {
  margin-bottom: 10px;
}
</style>
