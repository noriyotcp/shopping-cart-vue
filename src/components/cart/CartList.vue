<template>
  <div>
    <p class="lead">Product Cart</p>
    <table class="table">
      <thead class="thead-light">
        <tr>
          <th scope="col">Title</th>
          <th scope="col">Quantity</th>
          <th scope="col">Price</th>
          <th scope="col">Remove</th>
        </tr>
      </thead>
      <tbody>
        <cart-item v-for="item in cartItems" :key="item.id" :cart-item="item" />
      </tbody>
    </table>
    <hr/>
    <button class="btn btn-success btn-lg">
      Checkout
      <span>(${{ cartTotal }})</span>
    </button>
  </div>
</template>

<script>
import CartItem from './CartItem'
import { mapGetters } from 'vuex'

export default {
  name: 'CartList',
  components: {
    CartItem
  },
  created() {
    this.$store.dispatch('fetchCartItems')
  },
  computed: {
    ...mapGetters(['cartItems', 'cartTotal'])
  }
};
</script>
