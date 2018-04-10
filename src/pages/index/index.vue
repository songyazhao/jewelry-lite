<template>
  <div class="container">
    <section class="banner">
      <img src="/static/img/banner.jpg">
      <div class="rect">
        <img src="/static/img/logo.png">
      </div>
    </section>
    <XTitle icon-name="zs" text="产品展示" text-en="Product display"/>
    <XSwiper></XSwiper>
    <XTitle icon-name="jggc" text="加工过程" text-en="Workpiece process"/>
    <div class="product box-shadow" style="height: 138vw">
      <img src="/static/img/jiagong.png">
    </div>
    <XTitle icon-name="dz" text="定制流程" text-en="Custom process"/>
    <div class="custom">
      <div class="custom-img">
        <img src="/static/img/flow.png">
      </div>
      <div class="custom-con">
        <p>定制一颗有意义的钻石</p>
        <p>爱不仅是誓言</p>
        <p>更要用心行动</p>
        <p>缔造一生的承诺</p>
        <p>纵享恒久的情缘</p>
      </div>
    </div>
    <div class="product">
      <img src="/static/img/s.png">
    </div>
    <XTitle icon-name="gywm" text="关于我们" text-en="About company"/>
    <div class="about">
      <div class="about-con">
        <p>KALCOLOR高端珠宝定制是一个集款式设计、工艺制作、产品运营于一体的珠宝品牌，专注宝石、钻石等珠宝的高端定制，为每一个人量身打造最契合自身精气神的珠宝产品。</p>
        <p>作为一个年轻活力的珠宝定制品牌，KALCOLOR自创立以来，始终秉承着精益求精、臻于至善的宗旨，用独具匠心的设计演绎不同凡响，天马行空的幻想与绚丽多彩的现实互相碰撞所迸发的灵感，皆为KALCOLOR所捕捉，用珠宝来铭刻亲情、爱情、友情，让瞬间成为流传亘古的永恒，让珠宝诠释浪漫唯美的人生。KALCOLOR坚持只采用优质的宝石和材料，保证纯正的出品，每一件KALCOLOR珠宝的面世均需要经过重重磨炼，其制作工艺经得起考究，在香港镶嵌工艺的精心雕琢下得到进一步的升华。</p>
      </div>
      <div class="qrcode box-shadow">
        <img src="/static/img/qrcode.png">
      </div>
    </div>
    <div class="consult">
      <button @click="handleCall">我要咨询</button>
    </div>
  </div>
</template>

<script>
import XTitle from '@/components/x-title'
import XSwiper from '@/components/x-swiper'

export default {
  components: {
    XTitle,
    XSwiper
  },

  methods: {
    handleCall() {
      wx.makePhoneCall({
        phoneNumber: '15992200750'
      })
    }
  }
}
</script>

<style lang="stylus" scoped>
img {
  width: 100%;
  height: 100%;
}

.banner {
  position: relative;

  img {
    width: 100vw;
    height: 73.5vw;
  }

  .rect {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;

    img {
      position: absolute;
      width: 155px;
      height: 30px;
      z-index: 1;
    }

    img, &::before, &::after {
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }

    &::before, &::after {
      content: '';
      position: absolute;
      display: block;
      box-sizing: border-box;
    }

    &::before {
      width: 80%;
      height: 70%;
      border: 2px solid white;
    }

    &::after {
      width: 70%;
      height: 60%;
      background-color: rgba(255, 255, 255, 0.65);
    }
  }
}

.box-shadow {
  box-shadow: 0 15px 20px -10px rgba(0, 0, 0, 0.25);
}

.product {
  width: 100vw;
  height: 138vw;
}

.custom {
  &-img {
    width: 100vw;
    height: 42vw;
  }

  &-con {
    line-height: 22px;
    margin-top: 20px;
    text-align: center;
  }
}

.about {
  &-con {
    line-height: 19px;
    padding: 0 20px;
    margin-bottom: 35px;
    text-indent: 2em;
    text-align: justify;
    font-size: 12px;
  }

  .qrcode {
    margin: 0 auto;
    width: 80vw;
    height: 102.5vw;
  }
}

.consult {
  margin: 30px 0;

  button {
    border-radius: 26px;
    width: 200px;
    font-size: 14px;
    color: white;
    line-height: 52px;
    background-color: #b69d5d;
  }
}
</style>
