<template lang="pug">
div
  Section(main='特别鸣谢' bg='Sponsors')
  Subsection 冠名赞助
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-kuaishou.jpg")' alt='快手公司的 Logo')
    v-col
      h2 快手
      v-col.text-line-height-2
        | 快手是记录和分享大家生活的平台，每天产生上千万条原创新鲜视频
        br
        | 在这里，发现真实有趣的世界

  Subsection 特约赞助
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-qingcloud.jpg")' alt='青云公司的 Logo')
    v-col
      h2 青云 QingCloud
      v-col.text-line-height-2
        | 青云 QingCloud （北京青云科技股份有限公司）是一家具有广义云计算服务能力的平台级混合云 ICT 厂商和服务商，以软件定义为核心，致力于为企业用户提供自主可控、中立可靠、性能卓越、灵活开放的云计算产品与服务。
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
