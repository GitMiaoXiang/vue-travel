<template>
  <div>
    <home-header></home-header>
    <home-swiper :list="list"></home-swiper>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
export default {
  name: 'Home',
  components: {HomeSwiper, HomeHeader},
  data:function () {
    return {
      list:[
        {
          id:1,
          imgUrl:require('../../assets/images/1.png')
        },
        {
          id:2,
          imgUrl:require('../../assets/images/2.png')
        }
      ]
    }
  }
}
</script>

<style>
</style>
