<template lang="pug">
v-app
  Background
  Header(logo='HackPKU 2021' :fragments='fragments')

  v-main
    v-container
      Logo
      Introduction#Introduction
      Sponsors#Sponsors
      Awards#Awards
      Photos#Photos
      Arrangement#Arrangement
      Instruction#Instruction
      Questions#Questions

  v-footer(padless)
    v-container
      v-row
        v-col
          .d-flex.flex-column.flex-sm-row.justify-center.align-center
            v-img(
              :src='require("./assets/logo-eecs.webp")'
              alt='北大信科的 Logo'
              max-width='170px'
              height='150px'
              contain
            )
            .text-center.text-sm-left(style='line-height: 2') 北京大学信息科学技术学院
              br
              | 共青团北京大学信息科学技术学院
              br
              | 2021 © 北京大学信息科学技术学院学生会 HackPKU 2021 组委会
            .d-flex.flex-column.justify-center.align-center.ml-sm-4.mt-2.mt-sm-0
              b.text-h6.mb-2 特别鸣谢
              .d-flex.flex-wrap.justify-center.align-center
                v-img.logo(
                  :src='require("./assets/logo-kuaishou.webp")'
                  alt='快手公司的 Logo'
                  max-width='150px'
                  max-height='75px'
                  contain
                )
                v-img.logo(
                  :src='require("./assets/logo-qingcloud.webp")'
                  alt='青云公司的 Logo'
                  max-width='150px'
                  max-height='75px'
                  contain
                )
                v-img.logo(
                  :src='require("./assets/logo-tuyoo.webp")'
                  alt='途游公司的 Logo'
                  max-width='150px'
                  max-height='75px'
                  contain
                )
      v-row: v-col.text-center: a(href='https://beian.miit.gov.cn/') 京ICP备16004990号
</template>

<script>
import Header from './components/Header'
import Background from './components/Background'
import Logo from './components/Logo'
import Introduction from './components/Introduction'
import Sponsors from './components/Sponsors'
import Awards from './components/Awards'
import Photos from './components/Photos'
import Arrangement from './components/Arrangement'
import Instruction from './components/Instruction'
import Questions from './components/Questions'

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
    Questions,
  },

  data: () => ({
    fragments: [
      { fragment: '#Sponsors', name: '赞助商' },
      { fragment: '#Awards', name: '奖项设置' },
      { fragment: '#Photos', name: '往届风采' },
      { fragment: '#Arrangement', name: '赛程安排' },
      { fragment: '#Instruction', name: '选手须知' },
      { fragment: '#Questions', name: 'Q & A' },
    ],
  }),
}
</script>

<style lang="scss">
@media (min-width: 1264px) {
  .container {
    max-width: 1185px;
  }
  .logo {
    width: 100%;
    max-width: 400px;
  }
}
</style>
