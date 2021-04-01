<template lang="pug">
div
  Section(main='特别鸣谢' bg='Sponsors')
  Subsection 冠名赞助
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-kuaishou.webp")' alt='快手公司的 Logo')
    v-col
      h2 快手
      v-col.text-line-height-2
        | 快手是面向普通人的记录和分享生活的短视频社交平台。以“拥抱每一种生活”，用有温度的科技提升每个人独特的幸福感为核心使命。
        br
        | 经过多年发展，快手以成熟产品为基础，融合直播、电商、游戏、二次元等业务，不断拓展生态边界，旗下产品包括快手主 App 、快手极速版、快影、一甜相机、快看点、避风等，打造出领先的内容生态。

  Subsection 特约赞助
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-qingcloud.webp")' alt='青云公司的 Logo')
    v-col
      h2 青云 QingCloud
      v-col.text-line-height-2
        | 青云 QingCloud （北京青云科技股份有限公司）是一家具有广义云计算服务能力的平台级混合云 ICT 厂商和服务商，以软件定义为核心，致力于为企业用户提供自主可控、中立可靠、性能卓越、灵活开放的云计算产品与服务。
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-tuyoo.webp")' alt='途游公司的 Logo')
    v-col
      h2 途游游戏
      v-col.text-line-height-2
        | 途游游戏（Tuyoo Games) 成立于 2013 年，是中国领先的互动娱乐供应商，服务于全球十余亿用户，集移动游戏研发、运营、发行于一体。
        br
        | 途游拥有多项自主研发专利和数字智能技术。公司基于全球，围绕卡牌、休闲、消除三条产品线自研自发，产品包括：《捕鱼大作战》、《胡莱三国》小游戏、《途游斗地主》、《Panda Cube Smash》、《Fish Blast》、《Dream Home》、《Magnum Quest》、《Word Relax》、《Three Kingdoms & Puzzles》、《王国无敌》等多款移动游戏，多次获得全球主流应用商城推荐，屡次在政府部门、行业协会、专业媒体评选的奖项中获得殊荣。途游始终秉持 “让用户在游戏的世界更加快乐”的使命，持续创作绿色精品游戏，为全球用户提供优质精彩的娱乐服务，创造更加广泛的价值。目前已在北美、北京、深圳、长沙、江西等多地设立办公室。
</template>

<script>
import Section from './Section'
import Subsection from './Subsection'

export default {
  components: {
    Section,
    Subsection,
  },
}
</script>

<style scoped>
.text-line-height-2 {
  line-height: 2;
}
</style>
