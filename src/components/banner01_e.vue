<template>
    <div>
        <div class="swiper-container">
        <div class="swiper-slide" v-for="(value,key,index) in banlis" v-if="key == 0">
            <div>
                <p></p>
                <p><img :src="value.log01" /></p>
                <p>{{ value.name01 }}</p>
            </div>
            <div>
                <p class="grefont">{{ value.tit }}</p>
                <p class="redfont">{{ value.num }}</p>
                <p class="grefont">{{ value.cls }}</p>
            </div>
            <div>
                <p></p>
                <p><img :src="value.log02" /></p>
                <p>{{ value.name02 }}</p>
            </div>
        </div>
        </div>
        <!-- Add Pagination -->
        <div class="swiper-pagination01"></div>
        <!-- Add Arrows -->
        <div class="swiper-button-next01"></div>
        <div class="swiper-button-prev01"></div>
  </div>



</template>

<script>
import Swiper from 'swiper';
import 'swiper/dist/css/swiper.min.css';
export default {
   data(){
       return {
           banlis:[   
            {
               tit:'足协杯 决赛次回合', 
               cls:'集锦',
               log01:require("./img/tlo_01.png"),
               log02:require("./img/tlo_02.png"),
               num:'首回合 1 - 1',
               name01:'山东鲁能泰山',
               name02:'北京中赫国安'
            },
            {
               tit:'常规赛', 
               cls:'集锦',
               log01:require("./img/blog03.png"),
               log02:require("./img/blog04.png"),
               num:'117 - 86',
               name01:'开拓者',
               name02:'湖人'
            },
            {
               tit:'常规赛', 
               cls:'集锦',
               log01:require("./img/blog05.png"),
               log02:require("./img/blog06.png"),
               num:'106 - 86',
               name01:'北京',
               name02:'八一'
            },
            {
               tit:'常规赛', 
               cls:'集锦',
               log01:require("./img/blog07.png"),
               log02:require("./img/blog08.png"),
               num:'97 - 120',
               name01:'江苏',
               name02:'北控'
            }
           ]
       }
   },
   mounted:function(){
    this.$nextTick(function(){
    // var swiper = new Swiper('.swiper-container01', {
    //   slidesPerView: 2,
    //   spaceBetween: 10,
    //   slidesPerGroup: 1,
    //   loop: true,
    //   loopFillGroupWithBlank: true,
    //   pagination: {
    //     el: '.swiper-pagination01',
    //     clickable: true,
    //   },
    //   navigation: {
    //     nextEl: '.swiper-button-next01',
    //     prevEl: '.swiper-button-prev01',
    //   },
    // });

    })
  }
}
</script>
<style lang="scss" scoped>
@import "scss/base.scss";
    .swiper-container {
      width: 100%;
      height: 100%;
      padding-bottom:5px;
      background:#e6e6e6;
    }
    .swiper-wrapper{
        height: 100px;
    }
    .swiper-slide {
      text-align: center;
      font-size: 18px;
      background: #fff;
      color:#060606;
      width: 100%;
      float:left;
      /* Center slide text vertically */
      display: -webkit-box;
      display: -ms-flexbox;
      display: -webkit-flex;
      display: flex;
      -webkit-box-pack: center;
      -ms-flex-pack: center;
      -webkit-justify-content: center;
      justify-content: center;
      -webkit-box-align: center;
      -ms-flex-align: center;
      -webkit-align-items: center;
      align-items: center;
      border-radius: 0;
      margin-top:5px;
      height: 100px;
    }
    .swiper-slide:nth-child(2){
      float:right;
    }
    .swiper-slide:nth-child(4){
      float:right;
    }
    .swiper-slide div{
        display: block;
        clear: both;
        width: 100%;
        overflow: hidden;
        position: relative
    }
    .swiper-slide div p{
        line-height: 0.24rem;
    }
    .swiper-slide div p img{
        height: 0.41rem;
    }
    .swiper-container-horizontal{
        background:#fff;
        overflow: hidden;
        position: relative;
        z-index: 100;
    }
    .redfont{
        color:#d46d12
    }
    .grefont{
        color:#5b5b5b
    }
</style>