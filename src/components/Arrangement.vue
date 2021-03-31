<template lang="pug">
div
  Section(main="赛程安排" bg="Arrangement")
  v-timeline(dense)
    v-timeline-item(icon="mdi-account-plus" fill-dot :color="styles['decoration-color']" :large="!$vuetify.breakpoint.mobile")
      v-card
        v-card-title.grey.lighten-3 2021 年 4 月 2 日 至 4 月 15 日
        v-container
          v-col
            | 选手自行组队报名，依据模板填写简历并提交至 
            a(href="mailto:hackpku2021@126.com") hackpku2021@126.com
            |（详见下方 
            a(href="#Instruction") 选手须知
            |  ）
    v-timeline-item(icon="mdi-forum-outline" fill-dot :color="styles['decoration-color']" :large="!$vuetify.breakpoint.mobile")
      v-card
        v-card-title.grey.lighten-3 2021 年 5 月 5 日 至 5 月 7 日
        v-container
          v-col 赛前企业技术讲座与问答
    v-timeline-item(icon="mdi-code-tags" fill-dot :color="styles['decoration-color']" :large="!$vuetify.breakpoint.mobile")
      v-card
        v-card-title.grey.lighten-3 2021 年 5 月 8 日 12:00 至 5 月 10 日 12:00
        v-container
          v-list
            v-list-item 线上进行企业资源介绍与技术交流答疑 Workshop
            v-list-item 选手选定题目，利用相应材料在 48 小时内进行开发，完成相应要求并在线上提交通道关闭前提交相应文件
    v-timeline-item(icon="mdi-timer-sand-empty" fill-dot :color="styles['decoration-color']" :large="!$vuetify.breakpoint.mobile")
      v-card
        v-card-title.grey.lighten-3 2021 年 5 月 10 日 12:30 至 14:00
        v-container
          v-col 线上交流评分，优秀队伍进行展示准备
    v-timeline-item(icon="mdi-play-box-outline" fill-dot :color="styles['decoration-color']" :large="!$vuetify.breakpoint.mobile")
      v-card
        v-card-title.grey.lighten-3 2021 年 5 月 10 日 14:00 至 16:00
        v-container
          v-col 优秀作品展示与最终评分
    v-timeline-item(icon="mdi-license" fill-dot :color="styles['decoration-color']" :large="!$vuetify.breakpoint.mobile")
      v-card
        v-card-title.grey.lighten-3 2021 年 5 月 10 日 16:00 至 18:00
        v-container
          v-col 闭幕式与颁奖典礼
</template>

<script>
import Section from './Section'
import styles from '../scss/export.scss'

export default {
  components: {
    Section,
  },
  data() {
    return {
      styles,
    }
  },
}
</script>
