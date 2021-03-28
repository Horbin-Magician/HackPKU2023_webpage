<template lang="pug">
div
  Section(main="赞助商" bg="Sponsors")
  Subsection  顶级赞助商
  v-row.sponsor
    v-col.d-flex.align-center(cols="12" sm="4")
      v-img(:src="require('../assets/logo-mi.jpg')" alt="小米公司的 Logo")
    v-col
      h2 小米
      v-col.text-line-height-2
        | 小米公司正式成立于2010年4月，是一家专注于高端智能手机、互联网电视以及智能家居生态链建设的创新型科技企业。
        br
        |“让每个人都能享受科技的乐趣”是小米公司的愿景。小米公司应用了互联网开发模式开发产品的模式，用极客精神做产品，用互联网模式干掉中间环节，致力于让全球每个人，都能享用来自中国的优质科技产品。
  Subsection  二级赞助商
  v-row.sponsor
    v-col.d-flex.align-center(cols="12" sm="4")
      v-img(:src="require('../assets/logo-kuaishou.jpg')" alt="快手公司的 Logo")
    v-col
      h2 快手
      v-col.text-line-height-2
        | 快手是记录和分享大家生活的平台，每天产生上千万条原创新鲜视频
        br
        | 在这里，发现真实有趣的世界
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
.subsection::before {
  content: '%';
  background-color: #756ad6;
}
.subsection {
  margin-bottom: 10px;
}
.sponsor {
  margin-bottom: 1rem;
}
.text-line-height-2 {
  line-height: 2;
}
</style>
