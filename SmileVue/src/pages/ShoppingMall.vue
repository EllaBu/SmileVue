<template>
  <div>
    <div class="search-bar">
      <van-row>
        <van-col span="3" class="location-icon">
          <img src="../assets/images/location.png" alt="">
        </van-col>
        <van-col span="16">
          <input type="text" class="search-input">
        </van-col>
        <van-col span="5" class="search-btn">
          <van-button size="mini">查找</van-button>
        </van-col>
      </van-row>
    </div>
    <div class="swiper-area">
      <van-swipe :autoplay="3000">
        <van-swipe-item v-for="(banner, index) in bannerPicArr" :key="index">
          <img :src="banner.imageUrl" alt="">
        </van-swipe-item>
      </van-swipe>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ShoppingMall',
  data () {
    return {
      bannerPicArr: [
        {imageUrl: require('../assets/images/banner1.png')},
        {imageUrl: require('../assets/images/banner2.png')},
        {imageUrl: require('../assets/images/banner3.png')}
      ]
    }
  }
}
</script>

<style scoped>
  .search-bar {
    height: 1rem;
    background-color: #e5017d;
  }
  .search-input {
    width: 100%;
    height: .7rem;
    background-color: #e5017d;
    color: #fff;
    border-top: 0;
    border-left: 0;
    border-right: 0;
    border-bottom: 1px solid #fff;
  }
  .location-icon {
    /*padding-top: .01rem;*/
    text-align: center;
  }
  .location-icon img {
    width: .5rem;
    margin-top: -.25rem;
  }
  .search-btn {
    text-align: center;
  }
  .search-btn button {
    margin-top: -.5rem;
  }
  .swiper-area {
    width: 100%;
    clear: both;
  }
  .swiper-area img {
    width: 100%;
    height: 3rem;
  }
</style>
