<template lang="pug">
.d-flex.flex-column.align-stretch
  .d-flex.justify-space-around
    .ma-4.mb-4(v-for='x in number')
      .number {{ x }}
      v-divider
  .text-center {{ description }}
</template>

<script>
export default {
  props: {
    number: {
      type: Array,
      default: () => ['0'],
    },
    description: {
      type: String,
      default: '',
    },
  },
}
</script>

<style scoped lang="scss">
.number {
  color: $decoration-color;
  font-weight: 500;
  font-size: 45pt;
  transition: all ease 0.5s;
  padding: 0 10px;
}
.number:hover {
  transform: scale(1.2);
}
</style>
