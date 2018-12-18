<template>
  <div>
    <home-header :city = "city"></home-header>
    <home-swiper :list="swiperList"></home-swiper>
    <home-icons :list = "iconList"></home-icons>
    <home-recommend :list = "reList"></home-recommend>
    <home-weekend :list="weekList"></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
import axios from 'axios'
export default {
  name: 'Home',
  components: {HomeSwiper, HomeHeader, HomeIcons, HomeRecommend, HomeWeekend},
  data:function () {
    return {
      city: '',
      swiperList: [],
      iconList: [],
      reList: [],
      weekList: [],
    }
  },
  methods:{
    getHomeInfo (){
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc(res){
      res = res.data
      if(res.ret && res.data ){
        const data = res.data
        this.city = data.city
        this.swiperList = data.swiperList
        this.iconList = data.iconList
        this.reList = data.recommendList
        this.weekList = data.weekendList
      }

      console.log(res)
    }
  },
  mounted (){
    this.getHomeInfo()
  }
}
</script>

<style>
</style>
