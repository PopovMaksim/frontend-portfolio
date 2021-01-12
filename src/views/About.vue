<template>
  <AboutMe></AboutMe>

  <Experience></Experience>

</template>

<script>
import AboutMe from '@/components/AboutMe.vue'
import Experience from '@/components/Experience.vue'

export default {
  name: 'About',
  components: {
    AboutMe,
    Experience,
  }
}
</script>