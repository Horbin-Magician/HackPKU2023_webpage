<template lang="pug">
div
  Section(main='特别鸣谢' bg='Sponsors')
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-ubiquant.webp")' alt='九坤投资 Logo')
    v-col
      h2 九坤 Ubiquant
      v-col.text-line-height-2
        | 九坤投资于2012年4月成立，是一家以前沿科技持续驱动金融市场投资，致力于为投资者持续创造价值的量化对冲基金公司。目前资产管理规模超700亿元人民币，服务客户超过20000名，连续5年蝉联中国私募金牛奖，综合实力位居行业第一梯队。
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img.logo_huawei(
        :src='require("../assets/logo-huawei.webp")'
        alt='华为 Logo'
      )
    v-col
      h2 华为 Huawei
      v-col.text-line-height-2
        | 华为创立于1987年，是全球领先的ICT（信息与通信）基础设施和智能终端提供商。我们的20.7万员工遍及170多个国家和地区，为全球30多亿人口提供服务。我们致力于把数字世界带入每个人、每个家庭、每个组织，构建万物互联的智能世界。
        br
        | 科学探索与技术创新是推动人类文明进步和社会发展的主要力量。华为重视研究与创新，坚持走开放创新的道路，愿意与学术界、产业界一起，共同探索科学技术的前沿，推动创新升级，不断为全行业、全社会创造价值，携手共建美好的智能世界。 “让用户在游戏的世界更加快乐”的使命，持续创作绿色精品游戏，为全球用户提供优质精彩的娱乐服务，创造更加广泛的价值。目前已在北美、北京、深圳、长沙、江西等多地设立办公室。
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-zhenfund.webp")' alt='真格基金 Logo')
    v-col
      h2 真格 ZhenFund
      v-col.text-line-height-2
        | 作为国内最早的天使投资机构之一，真格基金自从2011年起长期投身于支持年轻优秀的创业者追寻自己的创新创业梦想，十余年来投资了数百家各个行业领域的创业公司，与创业者们共同打造从零到一的地基，见证和陪伴了一大批优秀的企业从青涩走向成熟的过程，目前在管资金规模超过120亿人民币。
  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-glodon.webp")' alt='广联达 Logo')
    v-col
      h2 广联达 Glodon
      v-col.text-line-height-2
        | 广联达科技股份有限公司作为数字建筑平台服务商，专注于建筑信息化行业20余年，始终定位于数字化使能者，在全球100多个国家和地区建立80余家分子公司，累计为行业36万家企业提供专业化服务。公司业务围绕工程项目的全生命周期，面向行管方、建设方、设计方、咨询方、施工方、设材厂商等产业链各参与方提供数字建筑全生命周期解决方案，以系统性的数字化能力推动建筑企业高质量发展。 ICT 服务商与数字化转型解决方案提供商，致力于通过一套自主创新、中立可靠、灵活开放的全维云平台为数字世界的高效运行提供坚实的基础支撑，加速推动百行千业数字化转型。

  v-row
    v-col.d-flex.align-center(cols='12' sm='4')
      v-img(:src='require("../assets/logo-tencent.webp")' alt='腾讯 Logo')
    v-col
      h2 腾讯 Tencent
      v-col.text-line-height-2
        | 腾讯是一家世界领先的互联网科技公司，用创新的产品和服务提升全球各地人们的生活品质。腾讯成立于1998年，总部位于中国深圳。公司一直秉承科技向善的宗旨。我们的通信和社交服务连接全球逾10亿人，帮助他们与亲友联系，畅享便捷的出行、支付和娱乐生活。腾讯发行多款风靡全球的电子游戏及其他优质数字内容，为全球用户带来丰富的互动娱乐体验。腾讯还提供云计算、广告、金融科技等一系列企业服务，支持合作伙伴实现数字化转型，促进业务发展。
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
.text-line-height-2 {
  line-height: 2;
}
.logo_huawei {
  max-width: 300px;
  margin: 0 auto;
}
</style>
