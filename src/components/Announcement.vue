<template lang="pug">
div
  Section(main='比赛公告' bg='Announcement')
  v-list(lines='one')
    v-list-item(
      v-for='announcement in announcements'
      :key='announcement.title'
    ) 
      v-list-item-content
        v-list-item-title {{ announcement.title }}
        v-list-item-subtitle {{ announcement.content }}
        v-list-item-subtitle {{ announcement.date }}
  v-list
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
          console.log(data)
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
    },
  },
}
</script>

<style scoped>
.text-line-height-2 {
  line-height: 2;
}
</style>
