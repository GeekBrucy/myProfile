<template>
  <div class="home">
    <about-me></about-me>
    <my-skills></my-skills>
    <my-projects></my-projects>
  </div>
</template>

<script>
import AboutMe from '../AboutMe/About'
import MySkills from '../Skills/Skills'
import MyProjects from '../Projects/Projects'

export default {
  name: 'Home',
  components: {
    AboutMe,
    MySkills,
    MyProjects
  }
}
</script>

<style lang="stylus" scoped>
</style>
