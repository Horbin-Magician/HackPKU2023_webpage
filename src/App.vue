<template lang="pug">
v-app
  Background
  Header(logo="HackPKU 2021" :fragments="fragments")

  v-main
    v-container
      Logo
      Introduction#Introduction
      Sponsors#Sponsors
      Awards#Awards
      Photos#Photos
      Arrangement#Arrangement
      Instruction#Instruction

  v-footer(padless)
    v-container
      v-row: v-col.text-center 2021 © 北京大学信息科学技术学院学生会 HackPKU 2021 组委会
      v-row: v-col.text-center: a(href="https://beian.miit.gov.cn/") 京ICP备16004990号
</template>

<script>
import Header from './components/Header'
import Background from './components/Background'
import Logo from './components/Logo'
import Introduction from './components/Introduction'
import Sponsors from './components/Sponsors'
import Awards from './components/Awards'
import Arrangement from './components/Arrangement'
import Instruction from './components/Instruction'

const Photos = () => import('./components/Photos')

export default {
  name: 'App',

  components: {
    Header,
    Background,
    Logo,
    Introduction,
    Sponsors,
    Awards,
    Photos,
    Arrangement,
    Instruction,
  },

  data: () => ({
    fragments: [
      { fragment: '#Sponsors', name: '赞助商' },
      { fragment: '#Awards', name: '奖项设置' },
      { fragment: '#Photos', name: '往届风采' },
      { fragment: '#Arrangement', name: '赛程安排' },
      { fragment: '#Instruction', name: '选手须知' },
    ],
  }),
}
</script>

<style lang="scss">
@media (min-width: 1264px) {
  .container {
    max-width: 1185px;
  }
}
</style>
