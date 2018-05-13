<template>
  <div class="about-me">
    <div class="section-overlay">
      <div class="container">
        <div class="about-left">
          <div class="photo"></div>
          <div class="social-media">
            <a href="https://github.com/GeekBrucy" target="blank"><i class="fab fa-github"></i></a>
          </div>
        </div>
        <div class="about-right">
          <h1>Hi All, I am Peichun Zhou</h1>
          <h3>Self-taught Front-end Developer</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquam, doloribus fugiat? Architecto porro sunt, quibusdam rerum impedit at cumque, a eos officiis optio provident hic delectus maiores totam laboriosam suscipit?Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit, veniam id nisi ut repellat sapiente quae. Sed optio nihil assumenda error aliquid laudantium illum. Animi adipisci libero voluptatem eius aliquid?Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis odit magnam omnis voluptates voluptatum commodi impedit! Sapiente in, excepturi debitis nulla reiciendis quisquam eaque ab possimus odio non deleniti aspernatur.</p>
          <div class="mylist">
            <ul class="title">
              <li>Working Right: </li>
              <li>Phone: </li>
              <li>Email: </li>
              <li>Location: </li>
            </ul>
            <ul class="content">
              <li>Australian Citizen</li>
              <li><a href="tel:+61420246599">+61420246599</a></li>
              <li><a href="mailto:peichunzhou1006@gmail.com">peichunzhou1006@gmail.com</a></li>
              <li>Latham, Canberra ACT 2615</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutMe'
}
</script>

<style lang="stylus" scoped>
.about-me
  background url(../../../static/imgs/section01.jpg) no-repeat
  background-size cover
  background-position center
  background-attachment fixed
  position relative
  min-height 600px
  .container
    z-index 999
    padding-top 1rem
    display flex
    min-height 600px
    .about-left
      padding 1rem .5rem
      flex 2
      .photo
        background url("https://image.ibb.co/fG5jMJ/ironmanflat.jpg") no-repeat
        background-position center
        background-size cover
        margin 0 auto
        width 70%
        height 70%
      .social-media
        width 70%
        margin 0 auto
        margin-top .5rem
        font-size .7rem
        text-align center
    .about-right
      padding 1rem
      flex 3
      h1
        font-size .8rem
        margin-bottom .4rem
      h3
        font-size .4rem
        margin-bottom .4rem
      p
        font-size .3rem
        margin-bottom .4rem
        line-height .4rem
      .mylist
        display flex
        font-size .4rem
        .title
          text-align left
          margin-right 1rem
        li
          padding .2rem 0
</style>
