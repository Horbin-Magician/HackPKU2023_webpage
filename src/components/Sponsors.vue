<template lang="pug">
div
  Section(main='特别鸣谢' bg='Sponsors')
  Subsection 独家冠名
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-kuaishou.webp")' alt='快手公司的 Logo')
    v-col
      h2 快手
      v-col.text-line-height-2
        | 快手是领先的内容社区和社交平台，是短视频行业开创者与引领者。全球范围内，快手是以平均日活跃用户数计第二大的短视频平台；以及以商品交易总额计第二大的直播电商平台。2021 年 2 月 5 日，快手科技（股票代码：1024.HK）在香港联交所主板挂牌上市。 我们致力于成为全球最痴迷于为客户创造价值的公司，帮助人们发现所需、发挥所长，持续提升每个人独特的幸福感。 经过 10 年发展，2021 年快手员工总数超过 2 万人，包括快手主 App、快手极速版、快影、一甜相机、快看点等在内，快手旗下产品矩阵进一步丰富，打造出领先的矩阵生态。

  Subsection 特约赞助
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-qingcloud.webp")' alt='青云公司的 Logo')
    v-col
      h2 青云科技 QingCloud
      v-col.text-line-height-2
        | 北京青云科技股份有限公司（简称：青云科技，股票代码：688316），混合云先行者与领导者，中国混合云第一股，是一家技术领先的企业级 ICT 服务商与数字化转型解决方案提供商，致力于通过一套自主创新、中立可靠、灵活开放的全维云平台为数字世界的高效运行提供坚实的基础支撑，加速推动百行千业数字化转型。
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-tuyoo.webp")' alt='途游公司的 Logo')
    v-col
      h2 途游游戏
      v-col.text-line-height-2
        | 途游游戏（Tuyoo Games）成立于 2013 年，是中国领先的互动娱乐供应商，服务于全球十余亿用户，集移动游戏研发、运营、发行于一体。
        br
        | 途游拥有多项自主研发专利和数字智能技术。公司自研自发多款移动游戏，多次获得全球主流应用商城推荐，屡次在政府部门、行业协会、专业媒体评选的奖项中获得殊荣。途游始终秉持 “让用户在游戏的世界更加快乐”的使命，持续创作绿色精品游戏，为全球用户提供优质精彩的娱乐服务，创造更加广泛的价值。目前已在北美、北京、深圳、长沙、江西等多地设立办公室。
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-hulu.webp")' alt='Hulu 公司的 Logo')
    v-col
      h2 Hulu
      v-col.text-line-height-2
        | Hulu 是美国领先的互联网专业视频服务平台，成立于 2006 年，目前由迪士尼控股，拥有超过 3800 万付费订阅用户，是全美用户数量增长最快的流媒体平台，原创内容屡获权威大奖。
        br
        | Hulu 总部位于美国洛杉矶，北京办公室成立于 2007 年，是仅次于总部的第二大研发中心，独立负责视频播放开发、内容推荐、广告投放等核心项目，在人工智能、机器学习等领域有专门的研究部门，拥有数十项专利。
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
