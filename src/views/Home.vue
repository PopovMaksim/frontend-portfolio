<template>
  <MainScreen />

  <AboutMe />

  <Works sub/>

  <WriteLetter page="home" />
</template>

<script>
// @ is an alias to /src
import MainScreen from '@/components/MainScreen.vue'
import AboutMe from '@/components/AboutMe.vue'
import Works from '../components/Works.vue'
import WriteLetter from '../components/WriteLetter.vue'



export default {
  name: 'Home',
  components: {
    MainScreen,
    AboutMe,
    Works,
    WriteLetter,
  }
}
</script>
