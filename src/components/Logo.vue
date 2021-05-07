<template lang="pug">
v-col.d-flex.flex-column.align-center
  v-img.logo(
    :src='require("../assets/logo.webp")'
    alt='HackPKU 2021 Logo'
    eager
  )
  .text-h2.text-sm-h1.mt-4.mb-16.text-center.text-line-height-1_2 第四届
    br.hidden-lg-and-up
    |
    | 北京大学
    br.hidden-md-and-up
    |
    | 新工科
    br
    | 黑客马拉松
  v-row
    v-col
      .text-h4.text-sm-h3.text-center
        | 本活动
        br.hidden-sm-and-up
        | 由快手独家赞助
  v-row
    v-col
      v-btn(
        :color='styles["decoration-color"]'
        dark
        large
        @click='downloadHandler'
      )
        v-icon(left) mdi-download
        | 赛题下载
      v-dialog(v-model='downloadDialog' max-width='300')
        v-card
          v-card-title 错误
          v-card-text {{ downloadDialogErrInfo }}
</template>

<script>
import styles from '../scss/export.scss'

export default {
  data() {
    return { styles, downloadDialog: false, downloadDialogErrInfo: '' }
  },
  methods: {
    downloadHandler() {
      fetch('/problemset')
        .then((response) => response.json())
        .then((response) => {
          if (response.code === 0) {
            const el = document.createElement('a')
            el.href = response.url
            el.download = 'problems.zip'
            el.click()
          } else {
            this.downloadDialogErrInfo = '比赛尚未开始，请耐心等待！'
            this.downloadDialog = true
          }
        })
        .catch(() => {
          this.downloadDialogErrInfo = '未知错误，请重试或联系工作人员！'
          this.downloadDialog = true
        })
    },
  },
}
</script>

<style scoped>
.logo {
  width: 100%;
  max-width: 400px;
}
.text-line-height-1_2 {
  line-height: 1.2;
}
</style>
