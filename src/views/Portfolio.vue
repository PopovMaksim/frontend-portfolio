<template>
  <h1 class="title">Портфолио</h1>
  <Works />
</template>

<script>
import Works from '../components/Works.vue'


export default {
  name: 'Portfolio',
  components: {
    Works,
  }
}
</script>