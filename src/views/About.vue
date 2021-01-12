<template>
  <h1 class="title">Обо мне</h1>
  
  <AboutMe></AboutMe>

  <Experience></Experience>

  <Skills></Skills>

</template>

<script>
import AboutMe from '@/components/AboutMe.vue'
import Experience from '@/components/Experience.vue'
import Skills from '@/components/Skills.vue'

export default {
  name: 'About',
  components: {
    AboutMe,
    Experience,
    Skills,
  }
}
</script>