<template>
  <div class="swiper_com">
    <swiper
      indicator-dots="true"
      indicator-color="#ccc"
      indicator-active-color="#f10215"
      autoplay="true"
      interval="5000"
      duration="100"
      circular="true"
      class="swiper_we"
    >
      <swiper-item class="item ">
        <view>
          <img src="./imgs/109951164569698464.jpg" alt>
        </view>
      </swiper-item>

      <swiper-item class="item">
        <view>
          <img src="./imgs/109951164569707867.jpg" alt>
        </view>
      </swiper-item>

      <swiper-item class="item">
        <view>
          <img src="./imgs/109951164569710428.jpg" alt>
        </view>
      </swiper-item>

      <swiper-item class="item">
        <view>
          <img src="./imgs/109951164569710929.jpg" alt>
        </view>
      </swiper-item>

      <swiper-item class="item">
        <view>
          <img src="./imgs/109951164570120827.jpg" alt>
        </view>
      </swiper-item>

      <swiper-item class="item">
        <view>
          <img src="./imgs/109951164570127246.jpg" alt>
        </view>
      </swiper-item>

      <swiper-item class="item">
        <view>
          <img src="./imgs/109951164570136055.jpg" alt>
        </view>
      </swiper-item>

      <swiper-item class="item">
        <view>
          <img src="./imgs/109951164570171019.jpg" alt>
        </view>
      </swiper-item>
      <swiper-item class="item">
        <view>
          <img src="./imgs/109951164570229032.jpg" alt>
        </view>
      </swiper-item>
    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  onLoad() {}
};
</script>

<style lang="less" scoped>
.swiper_com {
height: 150px;
  position: relative;
  padding:5px 15px;
  background: #fff;
}

.swiper_we .item img {
  display: block;
  width: 100%;
height: 170px;
  border-radius: 10px;
}
</style>
