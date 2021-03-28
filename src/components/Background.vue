<template lang="pug">
div.background
  div.decoration-block(v-for="_ in Array(20).keys()" :key="_")
  div.floating-char(v-for="char in floating_chars" :key="char") {{ char }}
</template>

<script>
export default {
  data() {
    return {
      floating_chars: '!@#$%&*()-+=[]{}?/<>~'.split(''),
    }
  },
}
</script>

<style lang="scss" scoped>
.background {
  position: absolute;
  pointer-events: none;

  width: 100%;
  height: 100%;

  background: #fafafa;

  overflow: hidden;
}

.decoration-block {
  position: absolute;
  transform: rotate(-45deg);
}

$decoration-blocks: 20;

@for $i from 1 through $decoration-blocks {
  $top: random();
  $scale: random();
  $greyscale: random(64) + 128 + 64;

  .decoration-block:nth-child(#{$i}) {
    width: 100% * $scale;
    height: 20 * $scale + px;
    background-color: rgb($greyscale, $greyscale, $greyscale);
    top: 100% * $top;
    @if random(2) == 1 {
      left: 0;
      transform-origin: left bottom;
    } @else {
      right: 0;
      transform-origin: right top;
    }
  }
}

.floating-char {
  font-size: 75pt;
  font-family: 'Source Code Pro', monospace;
  position: absolute;
  top: 0;
  transform-style: preserve-3d;
}

$floating-chars: 21;

@for $i from 1 through $floating-chars {
  $scale: random() + 0.5;

  .floating-char:nth-child(#{$i + $decoration-blocks}) {
    color: rgba(nth($monokai-colors, random(length($monokai-colors))), 0.5);
    left: random(120) * 1% - 20;
    animation: raise#{$i} 20 + random(20) + s linear infinite;
    animation-delay: random(40) - 40 + s;
    transform: scale($scale) rotate(random(360) + deg);
    z-index: 0;
    // filter: blur($i - 6 + px);

    @keyframes raise#{$i} {
      to {
        top: 100%;
        transform: scale($scale) rotate(random(720) + deg);
      }
    }
  }
}
</style>
