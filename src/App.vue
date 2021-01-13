<template>
  <Aside></Aside>
  <main class="main">
    <router-view/>

  </main>

  
</template>

<script>
  import Aside from '@/components/Aside.vue'

  export default {
    name: 'App',
    components: {
      Aside,
    },
  }
</script>

<style lang="scss">
  #app {
    display: grid;

    overflow: hidden;
    height: 100vh;

    transition: .3s;

    @media (max-width: 530px) {
      grid-template-columns: auto;
    }
    @media (min-width: 530px) {
      grid-template-columns: 3em auto;
    }
  }

  .main {
    position: relative;
    
    overflow-y: scroll;
    scroll-behavior: smooth;

    &::after {
      content: "";

      display: block;
      width: 100%;
      height: 10%;
    }
  }
</style>
