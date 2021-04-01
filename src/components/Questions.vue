<template lang="pug">
div
  Section(main='Q & A' bg='Q & A')
  v-card
    v-card-title.grey.lighten-3 Q：黑客马拉松是一个什么样的活动？
    v-container
      v-col A：黑客马拉松是一个短时间极限开发的挑战活动，选手们聚集在一起，几十个小时内不休不眠挑战开发，是软件开发者们的狂欢。
  <br/>
  v-card
    v-card-title.grey.lighten-3 Q：我在黑客马拉松活动中会收获什么？
    v-container
      v-col A：在这里，你不仅可以和伙伴们极限开发，锻炼团队活动，收获成就满足感，而且还可以和企业与高校的技术人员关于技术内容深入讨论，与天南海北的朋友讨论交流，享受赛前赛中的技术培训，以及收获到企业参访的机会，和自己心仪的企业更进一步。当然还有我们的比赛奖金等着大家！
  <br/>
  v-card
    v-card-title.grey.lighten-3 Q：本次比赛为线上比赛，具体会以怎样的形式开展呢？
    v-container
      v-col A：在之前的活动中，大由于疫情的原因，我们的比赛会调整为线上进行。报名、赛前培训、开幕签到、结果提交、技术交流均会以线上的方式完成，保证大家在疫情期间的安全。
  <br/>
  v-card
    v-card-title.grey.lighten-3 Q：线上比赛该如何保证比赛的公平性呢？
    v-container
      v-col A：组委会将设立公平监察机制，通过对源码进行审查、高校老师与企业技术人员提问等方式尽力保证比赛的公平性。同时我们将保证源码不会用于其他用途。
</template>

<script>
import Section from './Section'
import Subsection from './Subsection'
import styles from '../scss/export.scss'

export default {
  components: {
    Section,
    Subsection,
  },
  data() {
    return {
      styles,
    }
  },
}
</script>
