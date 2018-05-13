<template>
  <section class="my-project">
    <div class="project-header">
      My Projects
    </div>
    <div class="project-content">
      <div class="project-container">
        <div class="project-title">First Website</div>
        <div class="project-body">
          <a class="project-link" href="https://github.com/GeekBrucy/mywebsite">
            <div class="overlay">
              <p>
                This is my very first website, hosted on Digital Ocean. (Actually had a worse version, but previous host got DNS attack...anyway)
              </p>
            </div>
            <img src="../../../static/imgs/first_site.png" alt="">
          </a>
        </div>
      </div>
      <div class="project-container">
        <div class="project-title">Blog Website</div>
        <div class="project-body">
          <a class="project-link" href="https://github.com/GeekBrucy/Serious_Stuff/tree/master/mySite">
            <div class="overlay">
              <p>My first personalized blog website. Only authorized user can submit post, but everyone can comment. Markdown syntax supported.</p>
            </div>
            <img src="../../../static/imgs/first_blogsite.png" alt="">
          </a>
        </div>
      </div>
      <div class="project-container">
        <div class="project-title">PSD to HTML</div>
        <div class="project-body">
          <a class="project-link" href="https://github.com/GeekBrucy/front_end_drill/tree/practice/PSDtoHTML/nest_login">
            <div class="overlay">
              <p>The first PSD to HTML project, the hexagon almost killed the project. (PSD was from online, not my design)</p>
            </div>
            <img src="../../../static/imgs/psdtohtml.png" alt="">
          </a>
        </div>
      </div>
    </div>
    <div class="project-footer">There will be MORE!!!</div>
  </section>
</template>

<script>
export default {
  name: 'MyProjects'
}
</script>

<style lang="stylus" scoped>
.project-header
  font-weight bold
  font-size .8rem
  color #F33535
  text-align center
  line-height 1.6rem
  background-color #fff
.project-content
  display flex
  justify-content space-around
  padding .5rem 0
  .project-container
    width 6rem
    .project-title
      font-size .6rem
      font-weight bold
      text-align center
    .project-body
      .project-link
        display block
        position relative
        text-align center
        .overlay p
          margin-top .3rem
      .project-link:hover .overlay
        height 100%
        font-size .4rem
      img
        width 100%
.project-footer
  text-align center
  font-size .6rem
  margin-bottom .5rem
</style>
