<template>
  <section class="my-skills">
    <div class="skill-header">
      My Skills
    </div>
    <div class="skill-content">
      <div v-for="(item, value) of skills" :key="value">
        <div class="skill-content-title">{{handleKeyName(value)}}</div>
        <div class="skill-content-container" v-for="(value, key) of item" :key="key">
          <h1>{{ handleKeyName(key) }}</h1>
          <div class="progress-bar-outter">
            <div class="progress-bar-inner"
            :style="{'width': handleProgressBarWidth(value) + '%', 'background': 'linear-gradient(45deg,' + handleProgressBarBgc(value).color + ',' + handleProgressBarBgc(value).color2 + ' )'}">
              <div class="progress-text">{{ handleProgressBarWidth(value) + '%' }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MySkills',
  data () {
    return {
      inView: false,
      skills: {
        front_end: {
          css: {score: 80, color: '#0071B7', color2: '#26A9DF'},
          bootstrap: {score: 80, color: '#0C0437', color2: '#5A2A4E'},
          javascript: {score: 75, color: '#D2C044', color2: '#F1DA4E'},
          jQuery: {score: 70, color: '#172C45', color2: '#193556'},
          vuejs: {score: 70, color: '#41B883', color2: '#35495E'}
        },
        back_end: {
          python: {score: 70, color: '#407EAF', color2: '#FFDC54'},
          django: {score: 70, color: '#092E20', color2: '#fff'}
        },
        soft_skills: {
          communication: 85,
          leader_ship: 85,
          team_player: 85
        }
      }
    }
  },
  methods: {
    handleKeyName (item) {
      var arr = item.split('_')
      if (arr.length > 1) {
        return arr[0].toUpperCase() + ' ' + arr[1].toUpperCase()
      } else {
        return item.toUpperCase()
      }
    },
    handleProgressBarBgc (item) {
      return {color: item.color ? item.color : '#F33535', color2: item.color2 ? item.color2 : '#000'}
    },
    handleProgressBarWidth (item) {
      return this.inView ? item.score ? item.score : item : 0
    },
    handleScroll () {
      if (this.isElementInViewport(this.$el)) {
        this.inView = true
        window.removeEventListener('scroll', this.handleScroll)
      } else {
        this.inView = false
      }
    },
    isElementInViewport (el) {
      var rect = el.getBoundingClientRect()
      return (
        rect.top >= 0 &&
        rect.left >= 0 &&
        rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
        rect.right <= (window.innerWidth || document.documentElement.clientWidth)
      )
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
.skill-header
  font-weight bold
  font-size .8rem
  color #F33535
  text-align center
  line-height 1.6rem
  background-color #fff
.skill-content
  display flex
  justify-content space-around
  padding .5rem 0
  .skill-content-title
    font-size .6rem
    font-weight bold
  .skill-content-container
    padding .4rem 0
    width 8rem
    h1
      font-size .4rem
    .progress-bar-outter
      padding .1rem
      margin-top .2rem
      width 100%
      height .7rem
      background-color #fff
      position relative
      .progress-bar-inner
        height 100%
        background-color #0170BA
        transition width 2s
        .progress-text
          position absolute
          left 50%
          top 50%
          transform translate(-50%, -50%)
</style>
