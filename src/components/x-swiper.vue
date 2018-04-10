<template>
  <div class="swiper-container">
    <swiper :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
      <block v-for="(item, index) in imgUrls" :key="index">
        <swiper-item>
          <image :src="item" class="slide-image" width="355" height="150"/>
        </swiper-item>
      </block>
    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imgUrls: [
        '/static/img/1.jpg',
        '/static/img/2.jpg',
        '/static/img/3.jpg',
        '/static/img/4.jpg',
        '/static/img/5.jpg',
        '/static/img/6.jpg',
        '/static/img/7.jpg',
        '/static/img/8.jpg'
      ],
      indicatorDots: true,
      autoplay: true,
      interval: 5000,
      duration: 1000
    }
  }
}
</script>

<style lang="stylus" scoped>
.swiper-container {
  width: 78vw;
  height: 60vw;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
  border-radius: 20px;
  overflow: hidden;

  swiper {
    height: 100%;
  }
}
</style>