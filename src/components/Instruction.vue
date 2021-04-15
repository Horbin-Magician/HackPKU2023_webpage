<template lang="pug">
div
  Section(main='选手须知' bg='Instructions')
  v-row
    v-col
      Subsection 报名细则
      ol.details
        li 本次活动面向全国所有高校的本科生与研究生
        li 所有参赛者应于报名开始后下载简历模板，并完整填写相关信息
        li 
          | 所有参赛者需自行组成
          |
          b 3 至 5 人
          |
          | 的队伍，同一队伍所有队员简历及相关材料应添加至同一压缩包（
          |
          code .zip
          |
          | 格式）文件中，其文件名应体现所有队员姓名（如：
          code 张三_李四_王五.zip
          |
          | ）
        li
          | 各队伍自行选派一名队长，于
          |
          b 2021 年 4 月 23 日 24 时前
          |
          | 向
          |
          a(href='mailto:hackpku2021@126.com') hackpku2021@126.com
          |
          | 发送主题为 “HackPKU 2021 报名” 的邮件，并将上述压缩包添加至附件；HackPKU 2021 组委会将以邮件回复的方式确认邮件接收成功
        li 
          | 报名截止后，HackPKU 2021 组委会将进行筛选，并在 3 日内通过网站及微信公众号公示报名成功的队伍，向所有队伍报名所用邮箱发送通知邮件；报名成功的队伍应在收到通知邮件后
          |
          b 3 日内
          |
          | 回复以确认参加比赛，否则将被视为弃权，请及时查收
        li 如有其他报名相关问题，可通过邮件联系工作人员答疑
  v-row
    v-col
      Subsection 赛制说明
      ol.details
        li
          | 本次比赛为线上比赛，所有队伍应于
          |
          b 2021 年 5 月 8 日 10:30 至 11:00
          |
          | 完成线上签到，再次确认参加
          |
          b HackPKU 2021
        li
          b 2021 年 5 月 8 日 12:00
          |
          | 开发环节正式开始，HackPKU 2021 组委会将公布具体题目与相应材料，各队伍选定题目后进行为期
          |
          b 48 小时
          |
          | 的开发；其间参赛者可自行选择参与企业举办的相关 Workshop
        li
          b 2021 年 5 月 10 日 12:00
          |
          | 开发环节结束，材料提交通道关闭，各队伍应在此之前通过指定渠道上交题目要求的相应内容
        li
          | 开发结束后将进入线上交流评分环节，评委团就各队伍提交的相关材料与源代码同队员进行交流并打分，依各队伍分数产生第一轮成绩排名，取
          |
          b 前六名
          |
          | 作为优秀队伍进入复评
        li
          | 2021 年 5 月 10 日 16:00 举行闭幕式，优秀队伍进行公开项目展示，评委对其进行第二轮打分以得到各队伍
          |
          b 最终排名
          |
          | ，企业依最终排名结果颁奖
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
