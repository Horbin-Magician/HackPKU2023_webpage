<template lang="pug">
v-app
  Background
  Header(logo='HackPKU 2023' :fragments='fragments')

  v-main
    v-container
      Logo
      Introduction#Introduction
      Announcement#Announcement
      Awards#Awards
      Photos#Revision
      Arrangement#Arrangement
      Instruction#Instructions
      Questions#QA
      Sponsors#Sponsors
      MessageBoard#MessageBoard

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
              | 2023 © 北京大学信息科学技术学院学生会 HackPKU 2023 组委会
            .d-flex.flex-column.justify-center.align-center.ml-sm-4.mt-2.mt-sm-0
              b.text-h6.mb-2 特约赞助
              .d-flex.flex-wrap.justify-center.align-center
                v-img.logo(
                  :src='require("./assets/logo-ubiquant.webp")'
                  alt='九坤 Logo'
                  max-width='200px'
                  height='75px'
                  contain
                )
                v-img.logo(
                  :src='require("./assets/logo-huawei.webp")'
                  alt='华为 Logo'
                  max-width='200px'
                  height='75px'
                  contain
                )
                v-img.logo(
                  :src='require("./assets/logo-zhenfund.webp")'
                  alt='真格 Logo'
                  max-width='200px'
                  height='75px'
                  contain
                )
                v-img.logo(
                  :src='require("./assets/logo-glodon.webp")'
                  alt='广联达 Logo'
                  max-width='200px'
                  height='75px'
                  contain
                )
                v-img.logo(
                  :src='require("./assets/logo-hikecapital.webp")'
                  alt='山行 Logo'
                  max-width='200px'
                  height='75px'
                  contain
                )
                v-img.logo(
                  :src='require("./assets/logo-tencent.webp")'
                  alt='腾讯 Logo'
                  max-width='200px'
                  height='75px'
                  contain
                )
      v-row: v-col.text-center: a(href='https://beian.miit.gov.cn/') 京ICP备16004990号
</template>

<script>
import Header from './components/Header'
import Background from './components/Background'
import Logo from './components/Logo'
import Introduction from './components/Introduction'
import Announcement from './components/Announcement'
import Awards from './components/Awards'
import Photos from './components/Photos'
import Arrangement from './components/Arrangement'
import Instruction from './components/Instruction'
import Questions from './components/Questions'
import Sponsors from './components/Sponsors'
import MessageBoard from './components/MessageBoard'

export default {
  name: 'App',

  components: {
    Header,
    Background,
    Logo,
    Introduction,
    Announcement,
    Awards,
    Photos,
    Arrangement,
    Instruction,
    Questions,
    Sponsors,
    MessageBoard,
  },

  data: () => ({
    fragments: [
      { fragment: '#Announcement', name: '比赛公告' },
      { fragment: '#Awards', name: '奖项设置' },
      { fragment: '#Revision', name: '往届风采' },
      { fragment: '#Arrangement', name: '赛程安排' },
      { fragment: '#Instructions', name: '选手须知' },
      { fragment: '#QA', name: '问题解答' },
      { fragment: '#Sponsors', name: '特别鸣谢' },
      { fragment: '#MessageBoard', name: '答疑留言' },
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
