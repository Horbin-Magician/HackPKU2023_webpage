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

  v-col.text--secondary * 以上是单个赛道的奖金安排，若无特殊情况，每个赛道的奖金设置相同且互相独立
  v-col.text--secondary * 奖金按队伍分发，纪念品按参赛者分发
  br

  Subsection 参赛福利
  v-col.text-h5 企业workshop！
  v-col.text-h5 ——企业专家将为参赛选手开设赛前workshop，面对面分享技术细节
  v-col.text-h5 参访入场劵！
  v-col.text-h5 ——参赛选手将有机会进入腾讯、广联达等公司参访
  v-col.text-h5 更高的平台！
  v-col.text-h5 ——参赛选手将有机会参与华为黑客马拉松等赛事，同技术大佬华山论剑
  v-col.text-h5 企业的关注！
  v-col.text-h5 ——优秀选手将与大赛评委深入交流，受到大厂HR的追踪关注
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
</style>
