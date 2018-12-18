<template>
  <div>
    <home-header></home-header>
    <home-swiper :list="list"></home-swiper>
    <home-icons :list = "iconList"></home-icons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
export default {
  name: 'Home',
  components: {HomeSwiper, HomeHeader, HomeIcons, HomeRecommend, HomeWeekend},
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
      ],
      iconList:[
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/50/26ffa31b56646402.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1811/f6/e54fad3ea337b02.gif',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc:'旅游'
        },
        {
          id:1,
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc:'旅游'
        }
      ]
    }
  }
}
</script>

<style>
</style>
