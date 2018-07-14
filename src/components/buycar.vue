<template>
  <div class="buycar">
    <h2>购物车</h2>
    <dl v-for="item in index" :key="item.id" >
      <img v-bind:src="item.img"  alt=""/>
      <dt>标题:{{item.title}}</dt>
      <dd>价格:{{item.price}}</dd>
      <dd>
        <input  type="button" value="+" @click="changeItem({id:item.id,num:1})">
        {{item.number}}
        <input  type="button" value="-" @click="changeItem({id:item.id,num:-1})">
      </dd>
      <dd><input  type="button" value="删除" @click="removeItem({id:item.id})"></dd>
    </dl>
    <input type="button" value="清空购物车" @click="clearBuycar">
    <input type="button" value="结算">
  </div>
</template>
<script>
  import {mapActions,mapGetters} from 'vuex';
  export default{
    computed:mapGetters([
      'buycar',"index"
    ]),
    methods:mapActions([
      'changeItem','removeItem','clearBuycar'
    ]),
    

  }
</script>
<style>
  .buycar{
    margin: 50px;
  }
  h2{
    text-align:center;
  }
</style>