<template lang="pug">
div
  Section(main="活动介绍" bg="Introduction")
  v-col.text-line-height-2
    | 北京大学黑客马拉松活动是一个短时间的软件项目开发活动。本活动旨在给同学们提供一个进行技术交流的平台，以及接触业界实际问题的场景；为同学们提供一次尽可能接近真实的软件开发经历。
</template>

<script>
import Section from './Section'

export default {
  components: {
    Section,
  },
}
</script>

<style scoped>
.text-line-height-2 {
  line-height: 2;
}
</style>
