<template>
	<view id="detail" @click="clickDetail">
		这里是detail页面{{name}}
		<view>组件的基本使用，还差button和image</view>
		<view class="box">
			<view>
				<!--文本可选 -->
				<text :selectable="true">这里是detail页面{{name}}</text>
			</view>
			<view>
				<!-- 文本不可选 -->
				<text :selectable="false">这里是detail页面{{name}}</text>
			</view>
			<view>
				<!-- 默认空格  一个空格，默认大小-->
				<text :selectable="false">这里是detail页面 {{name}}</text>
			</view>
			<view>
				<!--ensp 中文字符空格一半大小  有几个空格就有几个位置，不过是字体大小的一半-->
				<text :selectable="false" space="ensp" class="ensp">这里是detail页面 {{name}}</text>
			</view>
			<view>
				<!--emsp 中文字符空格大小 有几个空格就有几个位置，跟字体一样大小 -->
				<text :selectable="false" space="emsp" class="emsp">这里是detail页面 {{name}}</text>
			</view>
			<view>
				<!--nbsp 根据字体设置的空格大小  一个空格，跟字体大小一样-->
				<text :selectable="false" space="nbsp" class="nbsp">这里是detail页面 {{name}}</text>
			</view>
		</view>
		<!-- 
				view元素等同于div 

					1.hover-class   string  元素被按下时的样式
					2.hover-stop-propagation  string  阻止hover-class冒泡
					3.hover-start-time	Number	50	按住后多久出现点击态，单位毫秒
					4.hover-stay-time	Number	400	手指松开后点击态保留时间，单位毫秒
		-->
		<!-- <view class="box" hover-class="boxActive">
			<view
				class="box-inner"
				hover-class="boxInnerActive"
				:hover-stop-propagation="true"
				:hover-start-time="10000"
				:hover-stay-time="10000"
			></view>
		</view>-->
		<view class="box">
			<button>我是一个按钮</button>
		</view>
		<view class="box">
			<image src="../../static/tabFont/fenlei.png"></image>
		</view>
	</view>
</template>
<script>
export default {
	data() {
		return {
			name: 'detail',
		};
	},
	methods: {
		clickDetail() {
			console.log('detail');
		},
	},
};
</script>
<style lang="scss" scoped>
#detail {
	font-size: 20px;
	text-align: center;
	line-height: 50px;
	color: darkcyan;
}
.box {
	width: 100%;
	height: 400px;
	background: #8b0000;
}

.emsp {
	font-size: 30px;
}

.ensp {
	font-size: 30px;
}

.nbsp {
	font-size: 30px;
}
.box-inner {
	width: 200px;
	height: 200px;
	background: green;
}
.boxInnerActive {
	background: pink;
}
.boxActive {
	background: skyblue;
}
</style>