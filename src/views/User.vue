<template>
  <div class="user">
    <h1>{{ this.$route.params.id }}</h1>
    <router-link :to="{name: 'first'}">first</router-link> |
    <router-link :to="{name: 'second'}">second</router-link>
    <transition name="shake" mode="out-in">
      <router-view/>
    </transition>
  </div>
</template>

<style scoped>
  .router-link-exact-active {
    font-size: 25px;
    color: red;
  }

  .shake-enter-active {
    animation: shake 1s linear;
    transform: translate3d(0, 0, 0);
    backface-visibility: hidden;
  }

  @keyframes shake {
    10% {
      transform: translate3d(-10px, 0px, 0);
    }

    20% {
      transform: translate3d(10px, 0px, 0);
    }

    30% {
      transform: translate3d(-10px, 0px, 0);
    }
  }

</style>
