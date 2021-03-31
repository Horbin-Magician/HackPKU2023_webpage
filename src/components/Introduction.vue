<template lang="pug">
div
  Section(main='活动介绍' bg='Introduction')
  v-col.text-line-height-2
    | 想体验一场别开生面的技术盛宴吗？
    br
    | 想感受无限接近真实的线上软件开发吗？
    br
    | 想了解真正的技术大咖们攻克难关的思路吗？
    br
    | HackPKU 就是专为你准备的平台！
    br
    br
    | 这是国内高校赛事历史最长的黑客马拉松比赛，在国内有着首屈一指的影响力；
    br
    | 这里有各色大厂带来的技术难题，从计算机视觉到语音分析，带你走进各色领域的技术前沿；
    br
    | 这里有资历丰富的评委为你指点难题，不管你是技术大神还是萌新小白，相信都能在这里得到不一样的体验
    br
    | 除此之外，我们还将提供企业参访的机会与丰厚的奖品。HackPKU，等你来。
    br
    | 由于疫情影响此次 HackPKU 赛事将在
    |
    b 线上进行
    |
    | ，我们会将所有的资源、参赛手册、纪念品等通过邮寄的方式送到选手手中，为大家提供最好的线上参赛体验。
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
