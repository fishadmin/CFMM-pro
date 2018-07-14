<template>
  <div>
    <a href="#" class="search">
			开启你的美食之旅...
		</a>
		<ul class="nav nav1">
			<li>
				<a href="#">
					<img src="/static/images/icon.jpg" />
					<p>最新推荐</p>
				</a>
			</li>
			<li>
				<a href="#">
					<img src="/static/images/icon1.jpg" />
					<p>热门菜谱</p>
				</a>
			</li>
			<li>
				<a href="#">
					<img src="/static/images/icon2.jpg" />
					<p>人气菜肴</p>
				</a>
			</li>
			<li>
				<a href="#">
					<img src="/static/images/icon3.jpg" />
					<p>优惠券</p>
				</a>
			</li>
		</ul>
		<div data-am-widget="titlebar" class="am-titlebar am-titlebar-default title" >
		    <h2 class="am-titlebar-title ">   积分菜品 </h2>
		    <nav class="am-titlebar-nav">
		        <a href="#more" class="">more &raquo;</a>
		    </nav>
		</div>
	    <ul data-am-widget="gallery" class="am-gallery am-avg-sm-2 am-avg-md-3 am-avg-lg-4 am-gallery-default product">
		      <li v-for="item of index" :key="item.id">
		        <div class="am-gallery-item">
		            <a href="#" class="">
		              <img v-bind:src="item.img"  alt=""/>
		              <h3 class="am-gallery-title">{{item.title}}</h3>
		              <div class="am-gallery-desc">
		              	<em>{{item.price}}</em>
						<router-link tag="i" class="am-icon-cart-plus" to="buycar" @click="bcar"></router-link>
		              </div>
		            </a>
		        </div>
		      </li>
		      
		 </ul>
    </div>
</template>

<script>
import {mapGetters} from "vuex";
    export default{
		   computed:mapGetters([
                "index"
                ]),
			props:{
				list:{
					type:Array,
					default:[{id:1,title:'暂无标题',price:'暂无描述'}]
				},
				dataName:{
					type:String,
					required:true
				}
			},
			methods:{
				bcar(){
					console.log(this.item)
				}
			}
		}
</script>

<style lang="">
    
</style>