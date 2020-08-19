<template>
  <div class="home">
    <h1>{{ counter }}</h1>
    <button @click="increment(20)">increment</button>
    <button @click="asyncIncremrnt(10)">increment</button>
    <h2>{{ cartItemsCount }}</h2>
  </div>
</template>

<script>
import { mapState, mapMutations, mapGetters, mapActions } from 'vuex'
export default {
  name: 'home',
  computed: {
    ...mapState({
      message: 'message',
      counter: 'counter',
      cartItems: 'cartItems',
    }),
    ...mapGetters([
      'cartItemsCount'
    ]),
  },
  methods: {
    ...mapMutations([
      'increment'
    ]),
    ...mapActions({
      asyncIncremrnt: 'increment'
    }),
  }
}
</script>
