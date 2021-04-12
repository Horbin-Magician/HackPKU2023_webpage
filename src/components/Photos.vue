<template lang="pug">
div
  Section(main='往届风采' bg='Past Revision')
  v-lazy(height='60vw' max-height='320px')
    Swiper(:options='swiper_options' @click-slide='handleClickSlide')
      .swiper-slide(v-for='photo in photos' :key='photo.key')
        img.swiper-lazy(
          :data-src='require(`../assets/photos/${photo.filename}`)'
          :alt='`关于 ${photo.description} 的照片`'
        )
        .swiper-lazy-preloader
  v-dialog(v-model='display_photo' max-width='900')
    v-card(v-if='display_photo')
      v-img(
        :lazy-src='require(`../assets/photos/${dialog_photo.filename}`)'
        :src='require(`../assets/photos/hd/${dialog_photo.filename}`)'
        :alt='`关于 ${dialog_photo.description} 的高清照片`'
      )
      //- v-card-title.text-center
      v-col.text-center.h3 {{ dialog_photo.description }}
  v-col.text--secondary * 左右{{ $vuetify.breakpoint.mobile ? "划" : "拖" }}动查看更多，点击查看大图
  v-row
    v-col.col-12.col-md-6
      Number(
        :number='["40+", "800+"]'
        description='过去 3 届 HackPKU 中，共有来自全国各地 40 余所高校的 800 余支各具特色的队伍报名并参加比赛，HackPKU 得到广大选手的一致好评'
      )
    v-col.col-6.col-md-3
      Number(
        :number='["30+"]'
        description='30 余家企业曾给予 HackPKU 大力支持，为选手提供技术产品、开发框架、参访安排等'
      )
    v-col.col-6.col-md-3
      Number(
        :number='["10 万"]'
        description='共有 30 余支队伍的 100 余名同学获奖，历届 HackPKU 累计奖金超过￥100,000'
      )
    v-col.col-12
      Number(
        :number='["1"]'
        description='HackPKU 2021 第 1 次线上举办，活动奖金更丰厚，活动形式更多样，更多“第一”，等你来创造……'
      )
</template>

<script>
import Section from './Section'
import Number from './Number'
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'
import 'swiper/css/swiper.css'

import photos from '../assets/photos/photos.json'

export default {
  components: {
    Section,
    Number,
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      swiper_options: {
        autoplay: true,
        loop: true,
        loopedSlides: 2,
        spaceBetween: 10,
        slidesPerView: 'auto',
        centeredSlides: true,
        preloadImages: false,
        lazy: true,
        watchSlidesVisibility: true,
      },
      photos,
      display_photo: false,
      dialog_photo: null,
    }
  },
  methods: {
    handleClickSlide(index, realIndex) {
      this.display_photo = true
      this.dialog_photo = this.photos[realIndex]
    },
  },
}
</script>

<style lang="scss" scoped>
.swiper-lazy-preloader {
  --swiper-theme-color: #{$decoration-color};
}
.swiper-slide {
  width: 90vw;
  max-width: 480px;
  height: 60vw;
  max-height: 320px;
}
.swiper-lazy {
  width: 90vw;
  max-width: 480px;
  height: 60vw;
  max-height: 320px;
  opacity: 0;
  transition: opacity 0.4s ease;
}
.swiper-lazy-loaded {
  opacity: 1;
}
</style>
