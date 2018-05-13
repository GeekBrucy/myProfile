<template>
  <div class="home">
    <about-me></about-me>
    <my-skills></my-skills>
  </div>
</template>

<script>
import AboutMe from '../AboutMe/About'
import MySkills from '../Skills/Skills'
export default {
  name: 'Home',
  components: {
    AboutMe,
    MySkills
  }
}
</script>

<style lang="stylus" scoped>
</style>
