<template lang="pug">
h1.mt-4.mb-2: slot
</template>

<style lang="scss" scoped>
h1::before {
  content: '%';
  color: white;
  background-color: $decoration-color;
}
</style>
