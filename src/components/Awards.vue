<template lang="pug">
div
  Section(main='奖项设置' bg='Award Settings')
  Subsection 现金奖池
  v-row 
    v-col(cols='12' sm='4')
      v-card
        v-card-title.yellow.darken-2.text-h4.d-flex.justify-end: b ￥20000
          .glow
        v-container: v-col.text-h5 第一名
    v-col(cols='12' sm='4')
      v-card
        v-card-title.blue-grey.lighten-3.text-h4.d-flex.justify-end: b ￥10000
          .glow
        v-container: v-col.text-h5 第二名
    v-col(cols='12' sm='4')
      v-card
        v-card-title.deep-orange.darken-2.text-h4.d-flex.justify-end: b ￥5000
          .glow
        v-container: v-col.text-h5 第三名
  v-row
    v-col(cols='12' sm='4')
      v-card
        v-card-title.grey.lighten-3.text-h4.d-flex.justify-end: b ￥2000
          .glow
        v-container: v-col.text-h5 第四名至第八名
    v-col(cols='12' sm='4')
      v-card
        v-card-title.special.white--text.d-flex.justify-end HackPKU 神秘礼品
          .glow
        v-container: v-col.text-h5 所有获奖者
    v-col(cols='12' sm='4')
      v-card
        v-card-title.special.white--text.d-flex.justify-end HackPKU 精美纪念礼包
        v-container: v-col.text-h5 所有参赛者

  v-col.text--secondary 
    | * 以上是单个赛道的奖金安排，若无特殊情况，每个赛道的奖金设置相同且互相独立
    br
    | * 奖金按队伍分发，纪念品按参赛者分发
  br

  Subsection 参赛福利
  v-col.text-line-height-2
    ol
      li
        b 企业workshop！
        br
        | 企业专家将为参赛选手开设赛前workshop，面对面分享技术细节
      li
        b 参访入场劵！
        br
        | 参赛选手将有机会进入九坤、华为、真格基金、广联达、腾讯等公司参访
      li
        b 更高的平台！
        br
        | 参赛选手将有机会参与华为黑客马拉松等赛事，同技术大佬华山论剑
      li
        b 企业的关注！
        br
        | 优秀选手将与大赛评委深入交流，受到大厂HR的追踪关注
      li
        b 校招&实习直通车！
        br
        | 优秀选手将有机会得到华为实习绿色通道、广联达校招直通卡等福利
</template>

<script>
import Section from './Section'
import Subsection from './Subsection'

export default {
  components: {
    Section,
    Subsection,
  },
}
</script>

<style lang="scss" scoped>
.glow {
  height: 50%;
  width: 30%;
  position: absolute;
  left: 0;
  top: 0;
  background: linear-gradient(
    -45deg,
    rgba(255, 255, 255, 0),
    rgba(255, 255, 255, 0) 54px,
    rgba(255, 255, 255, 0.3) 54px,
    rgba(255, 255, 255, 0.3) 67px,
    rgba(255, 255, 255, 0) 67px,
    rgba(255, 255, 255, 0) 73px,
    rgba(255, 255, 255, 0.1) 73px,
    rgba(255, 255, 255, 0.1) 75px,
    rgba(255, 255, 255, 0) 75px,
    rgba(255, 255, 255, 0) 89px,
    rgba(255, 255, 255, 0.3) 89px,
    rgba(255, 255, 255, 0.3) 99px,
    rgba(255, 255, 255, 0) 99px
  );
}
.special {
  background-color: $decoration-color;
}
.text-line-height-2 {
  line-height: 2;
}
</style>
