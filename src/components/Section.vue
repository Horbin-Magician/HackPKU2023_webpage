<template lang="pug">
.section-container
  .bg {{ bg }}
  .main {{ main }}
</template>

<script>
export default {
  props: {
    main: { type: String, default: '' },
    bg: { type: String, default: '' },
  },
}
</script>

<style lang="scss" scoped>
.section-container {
  position: relative;
  display: inline-block;
  width: calc(100% + 2px);
}
.bg {
  font-weight: 800;
  margin-left: 1rem;
  margin-bottom: 40px;
  margin-top: 64px;
  font-style: italic;
  z-index: 0;
  color: rgba($decoration-color, 0.5);
  mask: repeating-linear-gradient(
    -45deg,
    transparent,
    transparent 5px,
    black 5px,
    black 20px
  );
}
.main {
  font-weight: 500;
  position: absolute;
  left: 0;
  bottom: 0;
  z-index: 1;
  margin-bottom: calc(40px - 1rem);
  color: #000;
}
.main:hover {
  text-decoration: underline;
}
.main::before {
  content: '# ';
}
@media only screen and (max-width: 600px) {
  .bg {
    font-size: 3rem;
  }
  .main {
    font-size: 2.5rem;
  }
}
@media only screen and (min-width: 600px) {
  .bg {
    font-size: 4rem;
  }
  .main {
    font-size: 3rem;
  }
}
</style>
