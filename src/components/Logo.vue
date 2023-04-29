<template lang="pug">
v-col.d-flex.flex-column.align-center
  v-img.logo(
    :src='require("../assets/logo2.webp")'
    alt='HackPKU 2023 Logo'
    eager
  )
  .text-h2.text-sm-h1.mt-4.mb-16.text-center.text-line-height-1_2 第六届
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
      v-btn(
        :color='styles["decoration-color"]'
        dark
        large
        @click='downloadHandler("赛题")'
      )
        v-icon(left) mdi-download
        | 赛题下载
    v-col
      v-btn(
        :color='styles["decoration-color"]'
        dark
        large
        @click='downloadHandler("技术支持")'
      )
        v-icon(left) mdi-download
        | 技术支持
    v-col
      v-btn(
        :color='styles["decoration-color"]'
        dark
        large
        @click='downloadHandler("其他资料")'
      )
        v-icon(left) mdi-download
        | 其他资料
    v-dialog(v-model='errorDialog' max-width='400')
      v-card
        v-card-title 错误
        v-card-text {{ errorDialogErrInfo }}
    v-dialog(v-model='downloadDialog' max-width='400')
      v-card
        v-card-title {{ downloadDialogTitle }}
        v-divider
        v-card-text
          v-list
            v-list-item(v-for='file in files' :key='file.filename')
              v-row 
                v-col(cols='9') {{ file.filename }}
                v-col
                  v-btn(
                    :color='styles["decoration-color"]'
                    dark
                    small
                    :href='file.url'
                  ) 下载
</template>

<script>
import styles from '../scss/export.scss'

export default {
  data() {
    return {
      styles,
      files: [],
      errorDialog: false,
      errorDialogErrInfo: '',
      downloadDialog: false,
      downloadDialogTitle: '',
    }
  },
  methods: {
    downloadHandler(flag = '赛题') {
      this.files = []
      let root_url =
        'https://api.github.com/repos/lcpu-club/HackPKU2023_webpage/contents/files/'
      fetch(root_url + flag)
        .then((response) => response.json())
        .then((data) => {
          for (let i = 0, len = data.length; i < len; i++) {
            let file = {
              filename: data[i]['name'],
              size: data[i]['size'],
              url: data[i]['download_url'],
            }
            this.files.push(file)
          }
          if (this.files.length == 0) {
            this.errorDialogErrInfo =
              '比赛尚未开始或该文件尚未准备好，请耐心等待！'
            this.errorDialog = true
          } else {
            this.downloadDialogTitle = flag + '下载'
            this.downloadDialog = true
          }
        })
        .catch(() => {
          this.errorDialogErrInfo = '未知错误，请重试或联系工作人员！'
          this.errorDialog = true
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
