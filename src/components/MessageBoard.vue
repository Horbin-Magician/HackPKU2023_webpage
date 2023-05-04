<template lang="pug">
div
  Section(main='答疑留言' bg='Message Board')
  #gitalk-container
</template>

<script>
import Section from './Section'
import Subsection from './Subsection'
import styles from '../scss/export.scss'

import Gitalk from 'gitalk'
import 'gitalk/dist/gitalk.css'

export default {
  components: {
    Section,
    Subsection,
  },
  data() {
    return {
      styles,
    }
  },
  mounted() {
    this.init()
  },
  methods: {
    init() {
      var gitalk = new Gitalk({
        clientID: '0381668c42597aa39ecc',
        clientSecret: '8ba8d5c7c869d8722a82054bbcc2032f814b8cf2',
        repo: 'HackPKU2023_webpage',
        owner: 'lcpu-club',
        title: 'HackPKU2023_MessageBoard',
        id: 'MessageBoard',
        admin: ['Horbin-Magician'],
        distractionFreeMode: false, // Facebook-like distraction free mode
      })
      gitalk.render('gitalk-container')
    },
  },
}
</script>
