<template lang="pug">
div
  Section(main="奖项设置" bg="Awards Setting")
  v-row
    v-col
      br
      Subsection  奖池设置
      br
      v-row 
        v-col(cols="12" sm="4")
          v-card
            v-card-title.yellow.darken-2.text-h4.d-flex.justify-end: b ￥20000
              div.glow
            v-container: v-col.text-h5 第一名
        v-col(cols="12" sm="4")
          v-card
            v-card-title.blue-grey.lighten-3.text-h4.d-flex.justify-end ￥10000
              div.glow
            v-container: v-col.text-h5 第二名
        v-col(cols="12" sm="4")
          v-card
            v-card-title.deep-orange.darken-2.text-h4.d-flex.justify-end ￥5000
              div.glow
            v-container: v-col.text-h5 第三名
      v-row
        v-col(cols="12" sm="4")
          v-card
            v-card-title.grey.lighten-3.text-h5.d-flex.justify-end ￥3000
              div.glow
            v-container: v-col.text-h5 第四名至第六名
        v-col(cols="12" sm="4")
          v-card
            v-card-title.grey.lighten-3.text-h5.d-flex.justify-end ￥1500
              div.glow
            v-container: v-col.text-h5 第七名至第十名
        v-col(cols="12" sm="4")
          v-card
            v-card-title.special.white--text.d-flex.justify-end HACKPKU 2021 定制纪念品
            v-container: v-col.text-h5 所有参赛者
  
      v-col
        div.text--secondary * 排名奖品按队伍分发，纪念品按参赛者分发

      br
      Subsection  参赛福利
      br
      //- v-row
      //-   v-col(cols="12" sm="4")
      //-     v-card
      //-       v-card-title.special.white--text.d-flex.justify-end 参访赛事赞助企业的机会
      //-         div.glow
      //-       v-container: v-col.text-h5 所有参赛者
      //-   v-col(cols="12" sm="4")
      //-     v-card
      //-       v-card-title.special.white--text.d-flex.justify-end HACKPKU 2021 定制纪念品
      //-         div.glow
      //-       v-container: v-col.text-h5 所有参赛者
      //- v-col
      //-   div.text--secondary * 企业参访名单以最终与企业的协调为准
      br
      v-col.text-h5 所有参加比赛的选手都将有机会获得参访赛事赞助企业的机会
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
