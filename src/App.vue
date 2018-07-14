<template>
  <div id="app">
    <loading v-show="bLoading"></loading>
    <router-view></router-view>
    <footbar v-show="bFoot"></footbar>
  </div>
</template>

<script>
  
  import we from './components/we.vue'
  import footbar from './components/footbar.vue'
  import {mapGetters} from 'vuex'
  export default {
     components:{
      footbar,we
     },
     computed:mapGetters([
      'bFoot','bLoading'
  ]),
  watch:{
    $route(){
      // console.log('watch 变化了',this.$route.path);
      this.checkRoute(this.$route.path)
    }
  },
  mounted(){
    // console.log('mounted',this.$route.path);
    this.checkRoute(this.$route.path)
  },
  methods:{
    checkRoute(path){
      if(/\/|home|speak|we/.test(path)){
        this.$store.dispatch('SHOW_FOOT');
      }
      if(/member/.test(path)){
        this.$store.dispatch('SHOW_FOOT');
      }
      if(/login|reg|content/.test(path)){
        this.$store.dispatch('HIDE_FOOT');
      }
    }
  }
  
  }
</script>

<style lang="">

</style>
