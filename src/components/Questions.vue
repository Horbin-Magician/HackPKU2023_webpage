<template lang="pug">
div
  Section(main='问题解答' bg='Questions / Answers')
  v-row: v-col: v-card
    v-card-title.grey.lighten-3 Q：我们有哪些信息渠道？该怎样获取信息？
    v-container
      v-col A：本次大赛的信息渠道汇总如下：
        br
        ol
          li
            b 微信群： 这是本次赛事的主要通知渠道
            ol(type='a')
              li 一个通知群即选手总群，用于发布各种赛程消息。
              li 赛道通知&答疑群，每个赛道各一个，用于各赛道的答疑和勘误。
          li
            b 大赛官方网站：
            a(href='https://hackpku.com') https://hackpku.com
            ol(type='a')
              li 选手可以通过网站下载各种文件，例如建立、本手册、赛题和技术支持等。
              li 开闭幕式线上会议的录制文件也会上传到网站。
              li 自报名开始，网站每 24 小时更新一次各赛道目前报名队伍数，可供选手参考。
              li 赛程中的重要通告、临时通知等，都会在网站上公布。
          li
            b 微信公众号：HackPKU2023
            ol(type='a')
              li 发布赛事推送，包括报名、回顾等。
              li 赛程中的重要通告、临时通知等，都会在公众号上发布。
          li
            b 大赛指定邮箱：
            a(href='mailto:hackpku@outlook.com') hackpku@outlook.com
            ol(type='a')
              li 用于提交简历及开发成果。
              li 提交简历和开发成果后，我们也会通过该邮箱发送反馈。
          li
            b 选手联络员
            ol(type='a')
              li 在选手组织阶段，我们会安排专门的工作人员联系每支队伍的队长，这位工作人员就是该队伍的联络人。比赛过程中有任何问题得不到及时解决，都可以联系本小队的联络人。
  v-row: v-col: v-card
    v-card-title.grey.lighten-3 Q：本次比赛是开放式开发，怎样确保成绩真实、评奖公平？
    v-container
      v-col A：对于真实性与公平性，我们的做法有如下
        ol
          li 我们设置了两轮评分，其中第二轮评分需线上展示与答辩。评委会考察选手对本队伍项目的理解和认识，防止过多的借鉴甚至抄袭，保证作品的独创性。
          li 评分过程中，大赛学术委员会将组织代码查重。查重既包括各队伍间代码的比对，也包括基于互联网代码库的重复率判定。一旦发现雷同，即严肃处理。
          li 闭幕式结束后，我们设置了为期两天的申诉和复议时间。对本队伍或其他队伍成绩真实性有疑问的选手，可以提请查分、复议，申请和评委交流。
  v-row: v-col: v-card
    v-card-title.grey.lighten-3 Q：想参赛但是没有找到合适的队友怎么办？
    v-container
      v-col A：扫码进入官方组队群，与来自五湖四海的参赛者们自由组队，开启专属于你的HackPKU之旅！
        a(@click='showQR = true') 点击查看群二维码
  v-dialog(v-model='showQR' max-width='300')
    v-card
      v-card-title 官方组队群
      v-card-text
        v-img(
          :src='require("../assets/QR.webp")'
          alt='HackPKU 2023 Logo'
          contain
        )
</template>

<script>
import Section from './Section'
import Subsection from './Subsection'
import styles from '../scss/export.scss'

export default {
  components: {
    Section,
    Subsection,
  },
  data() {
    return {
      styles,
      showQR: false,
    }
  },
}
</script>
