<template>
  <div class="header">
    <div class="container">
      <div class="nav-brand inline-block">
        Peichun Zhou
      </div>
      <ul class="main-nav inline-block">
        <li class="nav-item">About Me</li>
        <li class="nav-item">Skills</li>
        <li class="nav-item">Posts</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
.header
  line-height 1.6rem
  background-color #F33535
  .container
    display flex
    justify-content space-between
    .nav-brand
      font-size .5rem
    .main-nav
      .nav-item
        display inline-block
        font-size .4rem
        margin 0 .4rem
</style>
