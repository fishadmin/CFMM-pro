<template>
    <div>
        <slider1></slider1>
        <list :list="list" :dataName="dataName"></list>
    </div>
</template>

<script>
    import slider1 from './slider1.vue';
    import list from './list.vue';
    import {mapGetters} from "vuex";
    export default{
        data(){
            return{
               dataName:'home',
               list:[]
            }
        },
        components:{
            slider1,list
        },
        computed:mapGetters([
            "index"
        ]),
        mounted(){
          	this.$http({
                url:'http://localhost:8000/home',
                method:'get',
                // withCredentials:true,//跨域凭证
            }).then((res)=>{
                this.$store.dispatch("Cindex",res.data)
                // console.log(this.index)
            }).catch((res)=>{
                // console.log(res)
            })
        }
    }
</script>

<style lang="">
    
</style>
