<template lang="pug">
div
  Section(main='选手须知' bg='Instructions')
  v-row
    v-col
      Subsection 报名细则
      ol.details
        li 本次活动面向全国所有高校的本科生与研究生。
        li 所有参赛者应于报名开始后下载简历模板，并完整填写相关信息。
        li 
          | 参赛选手请
          b 以队伍为单位
          | ，于
          b 5月1日0:00至5月15日24:00
          | 将简历发送至大赛指定邮箱
          a(href='mailto:hackpku@outlook.com') hackpku@outlook.com。
        li
          | 选手依据简历模板填写简历。简历分为
          b 个人部分与团队部分
          | 。每位选手都需填写简历的个人部分；只有队长需要填写简历的团队部分。
        li 
          | 请如实填写个人信息，确保联系方式有效。若无法及时与您取得联系，可能会影响参赛资格、成绩评定和奖金发放等。
        li 
          | 填写完简历后，请将其保存为（
          code .pdf
          b 格式）， 并和学生证双面照片放进同一个文件夹
          | 。简历和学生证照片均命名为
          b 【姓名】
          | 。文件夹命名为【大学名-姓名】。
        li
          | 队长收集本队所有队员的报名材料文件夹（包括自己），打包成一个（
          code .zip
          b 格式文件）
          | ，作为附件发送到大赛指定邮箱。邮件和zip格式附件均命名为【队名-报名材料】。
        li
          b 请注意：提交简历即表示您许可将简历中的信息提供给赛事主办方，用于与赛事相关的事项。您的简历可能被发送至部分赞助商的人事部门。除此以外，我们承诺不会以任何方式泄露简历中的信息。若您对个人信息安全问题有任何疑问，请联系大赛负责人[电话：18801365090].
        li 邮件发送成功后，我们将于24小时内发送反馈邮件到您的邮箱，请注意查收。若逾期未收到任何反馈（报名成功或简历不合要求），请咨询选手联络负责人[电话：18005971270]。
  v-row
    v-col
      Subsection 赛制说明
      ol.details
        | 本次比赛为赛道制，共设2个赛道，各赛道内容不同，独立评奖，选手按照赛道要求自行组队参赛。每个队伍只能参加一个赛道。
        br
        | 赛道介绍:
        li
        li
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

<style scoped>
.details {
  line-height: 2rem;
  padding-left: 2rem;
}
</style>
