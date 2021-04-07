<template lang="pug">
v-app-bar(app :color='`rgba(245, 245, 245, ${scrollY})`' elevate-on-scroll)
  .d-flex.justify-space-between.align-center(
    v-if='$vuetify.breakpoint.xs || $vuetify.breakpoint.sm'
    style='width: 100%'
  )
    v-app-bar-title
      v-btn(text href='#') {{ logo }}
    v-menu(offset-y)
      template(v-slot:activator='{ on, attrs }')
        v-btn(icon v-bind='attrs' v-on='on' aria-label='导航菜单')
          v-icon mdi-menu
      v-list
        v-list-item(
          v-for='fragment in fragments'
          :href='fragment.fragment'
          :key='fragment.fragment'
          link
        ) {{ fragment.name }}
  v-container.d-flex(v-else style='display: flex')
    v-app-bar-title
      v-btn(text href='#') {{ logo }}
    v-spacer
    v-btn(
      v-for='fragment in fragments'
      :href='fragment.fragment'
      :key='fragment.fragment'
      text
    ) {{ fragment.name }}
</template>

<script>
export default {
  props: {
    logo: { type: String, default: '' },
    fragments: { type: Array, default: () => [] },
  },
  data() {
    return {
      scrollY: window.scrollY,
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.scrollY = window.scrollY
    },
  },
}
</script>
