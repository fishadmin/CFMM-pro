<template>
    <div>
        <div class="am-tabs qiehuan nav2 am-tabs-bd" data-am-tabs>
			  <ul class="am-tabs-nav am-nav am-nav-tabs">
			    <li class="am-active"><a href="#">店铺介绍</a>
						<div class="am-active" id="tab1">
			                  妈妈厨房是一家24小时经营以港式粤菜为基础的中西融合菜，特聘香港融合菜大师主理，打造新派主题时尚餐厅。它专业的厨师团队，开发和研究新派融合菜，定期推出特色菜品，聘请专业艺术团队研发造型，让茉莉每一款菜品成为一件艺术品，让客人感受别样的饮食文化。
			    	</div>
					</li>
			    <li class="am-tabs-nav am-nav am-nav-tabs" @click><a href="#">建议留言</a>
							<div class="am-tab-panel  am-in am-active" id="tab2">
			          <input type="text" placeholder="姓名" class="tab-input" />
			          <input type="text" placeholder="电话" class="tab-input" />
			          <textarea placeholder="建议" class="tab-input"></textarea>
			          <button type="button" class="tab-btn">提交</button>
			    	</div>
					</li>
			  </ul>
		
		</div>
    </div>
</template>

<script>
export default{
	
}
</script>