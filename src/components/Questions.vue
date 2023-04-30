<template lang="pug">
div
  Section(main='问题解答' bg='Questions / Answers')
  v-row: v-col: v-card
    v-card-title.grey.lighten-3 Q：我们有哪些信息渠道？该怎样获取信息？
    v-container
      v-col A：本次大赛的信息渠道汇总如下：
        br
        b (1) 微信群： 这是本次赛事的主要通知渠道
        ol
          li 一个通知群即选手总群，用于发布各种赛程消息。
          li 赛道通知&答疑群，每个赛道各一个，用于各赛道的答疑和勘误。
        br
        b (2) 大赛官方网站：
        a(href=':http://hackpku.fluctus.cc') http://hackpku.fluctus.cc
        ol
          li 选手可以通过网站下载各种文件，例如建立、本手册、赛题和技术支持等。
          li 开闭幕式线上会议的录制文件也会上传到网站。
          li 自报名开始，网站每 24 小时更新一次各赛道目前报名队伍数，可供选手参考。
          li 赛程中的重要通告、临时通知等，都会在网站上公布。
        br
        b (3) 微信公众号：Hack PKU（请注意空格和大小写）
        ol
          li 发布赛事推送，包括报名、回顾等。
          li 赛程中的重要通告、临时通知等，都会在公众号上发布。
        br
        b (4) 大赛指定邮箱：
        a(href='mailto:hackpku@outlook.com') hackpku@outlook.com
        ol
          li 用于提交简历及开发成果。
          li 提交简历和开发成果后，我们也会通过该邮箱发送反馈。
        br
        b (5) 选手联络员
        ol
          li 在选手组织阶段，我们会安排专门的工作人员联系每支队伍的队长，这位工作人员就是该队伍的联络人。比赛过程中有任何问题得不到及时解决，都可以联系本小队的联络人。
  v-row: v-col: v-card
    v-card-title.grey.lighten-3 Q：本次比赛是开放式开发，怎样确保成绩真实、评奖公平？
    v-container
      v-col A：对于真实性与公平性，我们的做法有如下
        ol(:type='1')
        li 我们设置了两轮评分，其中第二轮评分的形式是线上展示与答辩。评委会考察选手对本队伍项目的理解和认识，防止过多的借鉴甚至抄袭，保证作品的独创性。
        li 在评分过程中，大赛学术委员会将组织代码查重。查重既包括各队伍之间代码的比对，也包括基于互联网代码库的重复率判定。一旦发现雷同，即严肃处理。
        li 闭幕式结束后，我们设置了为期两天的申诉和复议时间。对本队伍成绩有疑问或对其他队伍成绩真实性有疑问的选手，可以提请查分、复议，申请和评委交流。
  v-row: v-col: v-card
    v-card-title.grey.lighten-3 Q：想参赛但是没有找到合适的队友怎么办？
    v-container
      v-col A：扫码进入官方组队群，与来自五湖四海的参赛者们自由组队，开启专属于你的HackPKU之旅！
  v-row: v-col: v-card
    v-card-title.grey.lighten-3 Q：黑客马拉松是一个什么样的活动？
    v-container
      v-col A：黑客马拉松是一个短时间极限开发的挑战活动，选手们聚集在一起，几十个小时内不休不眠挑战开发，是软件开发者们的狂欢。
  v-row: v-col: v-card
    v-card-title.grey.lighten-3 Q：我在黑客马拉松活动中会收获什么？
    v-container
      v-col A：在这里，你不仅可以和伙伴们极限开发，锻炼团队活动，收获成就满足感，而且还可以和企业与高校的技术人员关于技术内容深入讨论，与天南海北的朋友讨论交流，享受赛前赛中的技术培训，以及收获到企业参访的机会，和自己心仪的企业更进一步。当然还有我们的比赛奖金等着大家！
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
    }
  },
}
</script>
