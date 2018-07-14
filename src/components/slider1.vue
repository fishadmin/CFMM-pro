<template>
    <swipe class="my-swipe m1" :speed="200" :auto="2000">
      <swipe-item class="slide1"><img src="/static/images/banner.jpg"></swipe-item>
      <swipe-item class="slide2"><img src="/static/images/banner1.jpg"></swipe-item>
    </swipe>
</template>
<script>
  import '../../node_modules/vue-swipe/dist/vue-swipe.css';
  import { Swipe, SwipeItem } from 'vue-swipe';
  export default{
    components: {
      'swipe': Swipe,
      'swipe-item': SwipeItem
    }
  }
</script>
<style lang="">
  .m1 {
    height: 290px;
    color: #fff;
    font-size: 30px;
    text-align: center;
  }
  
  .slide1 {
    color: #fff;
  }
  
  .slide2 {
    color: #000;
  }
  
</style>