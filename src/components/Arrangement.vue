<template lang="pug">
div
  Section(main='赛程安排' bg='Arrangement')
  v-timeline(dense)
    v-timeline-item(
      icon='mdi-account-plus'
      fill-dot
      :color='styles["decoration-color"]'
      :large='!$vuetify.breakpoint.mobile'
    )
      v-card
        v-card-title.grey.lighten-3 2023 年 5 月 5 日 00:00 至 5 月 15 日 24:00
        v-container
          v-col
            | 选手自行组队报名，依据模板填写简历并提交至
            |
            a(href='mailto:hackpku@outlook.com') hackpku@outlook.com
            | （详见下方
            |
            a(href='#Instruction') 选手须知
            |
            | ）
    v-timeline-item(
      icon='mdi-account-group-outline'
      fill-dot
      :color='styles["decoration-color"]'
      :large='!$vuetify.breakpoint.mobile'
    )
      v-card
        v-card-title.grey.lighten-3 2023 年 5 月 16 日 至 5 月 18 日
        v-container
          v-col
            | 赛事主办方联络选手
    v-timeline-item(
      icon='mdi-ribbon'
      fill-dot
      :color='styles["decoration-color"]'
      :large='!$vuetify.breakpoint.mobile'
    )
      v-card
        v-card-title.grey.lighten-3 2023 年 5 月 20 日 08:00 至 10:00
        v-container
          v-col
            | 选手签到并举行开幕式
    v-timeline-item(
      icon='mdi-code-tags'
      fill-dot
      :color='styles["decoration-color"]'
      :large='!$vuetify.breakpoint.mobile'
    )
      v-card
        v-card-title.grey.lighten-3 2023 年 5 月 20 日 10:00 至 5 月 21 日 24:00
        v-container
          v-list
            v-list-item 选手利用相应材料在前 36 小时内进行开发，完成相应要求并在提交通道关闭前提交相应文件
    v-timeline-item(
      icon='mdi-play-box-outline'
      fill-dot
      :color='styles["decoration-color"]'
      :large='!$vuetify.breakpoint.mobile'
    )
      v-card
        v-card-title.grey.lighten-3 2023 年 5 月 22 日 至 5 月 24 日
        v-container
          v-col 第一轮评分
    v-timeline-item(
      icon='mdi-timer-sand-empty'
      fill-dot
      :color='styles["decoration-color"]'
      :large='!$vuetify.breakpoint.mobile'
    )
      v-card
        v-card-title.grey.lighten-3 2023 年 5 月 25 日 至 5 月 26 日
        v-container
          v-col 优秀队伍做展示准备
    v-timeline-item(
      icon='mdi-play-box-outline'
      fill-dot
      :color='styles["decoration-color"]'
      :large='!$vuetify.breakpoint.mobile'
    )
      v-card
        v-card-title.grey.lighten-3 2023 年 5 月 27 日
        v-container
          v-col 优秀作品展示与答辩（最终评分）
    v-timeline-item(
      icon='mdi-license'
      fill-dot
      :color='styles["decoration-color"]'
      :large='!$vuetify.breakpoint.mobile'
    )
      v-card
        v-card-title.grey.lighten-3 2023 年 5 月 27 日
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
