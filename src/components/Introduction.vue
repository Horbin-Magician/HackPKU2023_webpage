<template lang="pug">
div
  Section(main='活动介绍' bg='Introduction')
  v-col.text-line-height-2
    | 想体验一场别开生面的技术盛宴吗？
    br
    | 想感受无限接近真实的软件开发吗？
    br
    | 想了解真正的技术大咖们攻克难关的思路吗？
    br
    | 黑客马拉松（HackPKU）就是专为你准备的平台！
    br
    br
    b 什么是黑客马拉松？什么是HackPKU？
    br
    | 黑客马拉松（Hackathon），又称编程马拉松，
    br
    | 是指一群热爱技术、热爱设计的人聚集在一起，以小队合作的形式在几十个小时内完成某个创新项目或者创意设计的活动。
    br
    | HackPKU是国内高校赛事历史最长的黑客马拉松比赛，在国内有着首屈一指的影响力；
    br
    | 这里有各色大厂、顶尖高校带来的技术难题，从计算机视觉到语音分析，带你走进各色领域的技术前沿；
    br
    | 这里有资历丰富的评委为你指点迷津。不管你是技术大神还是萌新小白，相信都能在这里得到不一样的体验。
    br
    | HackPKU 2023 等你来!!!
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
