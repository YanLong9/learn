<template>
	<view id="list" @click="clickList">
		这里是list页面{{name}}
		<view class="box"></view>
	</view>
</template>
<script>
export default {
	data() {
		return {
			name: 'list',
		};
	},
	methods: {
		clickList() {
			console.log('list');
		},
	},
};
</script>
<style lang="scss" scoped>
#list {
	font-size: 20px;
	text-align: center;
	line-height: 50px;
	color: darkcyan;
}
.box {
	width: 100%;
	height: 2000px;
	background: darkolivegreen;
}
</style>