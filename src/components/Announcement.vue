<template lang="pug">
div
  Section(main='比赛公告' bg='Announcement')
  v-expansion-panels(focusable v-model='panel')
    v-expansion-panel(
      v-for='announcement in announcements'
      :key='announcement.title'
    )
      v-expansion-panel-header
        b {{ announcement.title }} {{ announcement.date }}
      v-expansion-panel-content
        .text-line-height-2(v-html='announcement.content')
</template>

<script>
import Section from './Section'

export default {
  components: {
    Section,
  },
  data() {
    return {
      announcements: [],
      panel: 0,
    }
  },
  mounted() {
    this.init()
  },
  methods: {
    init() {
      fetch(
        'https://hackpku.obs.cn-north-4.myhuaweicloud.com/Announcement.json'
      )
        .then((response) => response.json())
        .then((data) => {
          console.log(data)
          for (let i = 0, len = data.length; i < len; i++) {
            this.announcements.push({
              title: data[i]['title'],
              content: data[i]['content'],
              date: data[i]['date'],
            })
          }
        })
    },
  },
}
</script>

<style scoped>
.text-line-height-2 {
  line-height: 2;
}
</style>
