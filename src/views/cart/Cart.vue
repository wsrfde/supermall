<template>
  <div class="cart">
    <nav-bar class="nav-bar">
      <div slot="center">
        购物车({{length}})
      </div>
    </nav-bar>
    <cart-list></cart-list>
  </div>
</template>

<script>
  import NavBar from "components/common/navbar/NavBar";
  import CartList from "./childComps/CartList";

  import {mapGetters} from 'vuex'

  export default {
    name: "Cart",
    components: {
      NavBar,
      CartList
    },
    computed:{
      ...mapGetters({
        length:'cartLength'
      })
    }
  }
</script>

<style scoped>
  .nav-bar{
    background: var(--color-tint);
    color: #ffffff;
  }
</style>
