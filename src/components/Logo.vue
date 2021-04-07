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
        link
        href='https://7465-test-5gifm62t1406c277-1253429680.tcb.qcloud.la/HackPKU2021_%E7%AE%80%E5%8E%86%E6%A8%A1%E6%9D%BF.docx?sign=dcf779f161e6c57a8a27421ae13aa617&t=1616781245'
      ) 下载报名简历模板
</template>

<script>
import styles from '../scss/export.scss'

export default {
  data() {
    return { styles }
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
