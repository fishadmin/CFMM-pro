<template>
	<div>
    <div class="h50"></div>
		<div data-am-widget="navbar" class="am-navbar am-cf am-navbar-default footer "  id="">
		      <ul class="am-navbar-nav am-cf am-avg-sm-4">
					<router-link tag="li" to="home">
						<a href="javascript:;" class="">
							<span class=""><img src="/static/images/nav.png"/></span>
							<span class="am-navbar-label">点餐</span>
						</a>
					</router-link>
		        	<router-link tag="li" to="speak">
						<a href="javascript:;" class="">
							<span class=""><img src="/static/images/nav2.png"/></span>
							<span class="am-navbar-label">客说</span>
						</a>
					</router-link>
		          	<router-link tag="li" to="we">
						<a href="javascript:;" class="">
							<span class=""><img src="/static/images/nav3.png"/></span>
							<span class="am-navbar-label">我们</span>
						</a>
					</router-link>
		          	<router-link tag="li" to="user">
						<a href="javascript:;" class="">
							<span class=""><img src="/static/images/nav4.png"/></span>
							<span class="am-navbar-label">我的</span>
						</a>
					</router-link>
		      </ul>
		</div>
		</div>
</template>

<script>
	export default {
	}
</script>