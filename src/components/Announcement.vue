<template lang="pug">
div
  Section(main='比赛公告' bg='Announcement')
  v-card(lines='one')
    v-list-item(
      v-for='announcement in announcements'
      :key='announcement.title'
    ) 
      v-list-item-content
        v-list-item-title {{ announcement.title }} {{ announcement.date }}
        v-list-item-subtitle {{ announcement.content }}
    v-list-item(v-if='announcements.length == 0'): v-col.text-center 暂无公告
</template>

<script>
import Section from './Section'

export default {
  components: {
    Section,
  },
  data() {
    return { announcements: [] }
  },
  mounted() {
    this.init()
  },
  methods: {
    init() {
      fetch(
        'https://api.github.com/repos/Horbin-Magician/HackPKU2023_webpage/issues/3/comments'
      )
        .then((response) => response.json())
        .then((data) => {
          for (let i = 0, len = data.length; i < len; i++) {
            let date = data[i]['updated_at']
            let message = data[i]['body'].split('\r\n')
            let title = message[0]
            let content = message[1]
            this.announcements.push({
              title: title,
              content: content,
              date: date,
            })
          }
        })
      // this.announcements = [
      //   {
      //     title: '第一条公告',
      //     content: '这是第一条公告',
      //     date: '20230502',
      //   },
      //   {
      //     title: '第二条公告',
      //     content: '这是第二条公告',
      //     date: '20230503',
      //   },
      // ]
    },
  },
}
</script>

<style scoped>
.text-line-height-2 {
  line-height: 2;
}
</style>
