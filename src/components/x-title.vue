<template>
  <div class="title">
    <div class="title-icon">
      <img :src="_iconName">
    </div>
    <div class="title-con">
      <div class="en">{{ textEn }}</div>
      <div class="zh-cn">{{ text }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['iconName', 'text', 'textEn'],

  computed: {
    _iconName() {
      return `/static/img/${this.iconName}.png`
    }
  }
}
</script>

<style scoped lang="stylus">
img {
  width: 100%;
  height: 100%;
}

.title {
  margin-top: 40px;
  margin-bottom: 30px;
  display: flex;
  align-items: center;
  position: relative;

  &::before, &::after {
    content: '';
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    display: inline-block;
    height: 1px;
    width: 50px;
    background-color: #3E3E3E;
  }

  &::before {
    left: -70px;
  }

  &::after {
    right: -70px;
  }

  &-icon {
    width: 25px;
    height: 25px;
    // margin-top: 5px;
  }

  &-con {
    margin-left: 0.5em;

    .en {
      font-size: 0.5em;
      font-family: 'simsun';
    }

    .zh-cn {
      font-family: 900;
      color: #3E3E3E;
    }
  }
}
</style>
