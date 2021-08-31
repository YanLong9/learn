<template>
  <view id="cssScss" @click="clickCssScss">
    这里是cssScss页面{{name}}
    <view class="box">
      <!-- 
                uniapp的样式与布局

                1.单位  uniapp支持的通用 css 单位包括 px、rpx

                    px     即屏幕像素
                    rpx    即响应式px，一种根据屏幕宽度自适应的动态单位。以750宽的屏幕为基准，750rpx恰好为屏幕宽度。屏幕变宽，rpx 实际显示效果会等比放大。
                    rem    默认根字体大小为 屏幕宽度/20（微信小程序、字节跳动小程序、App、H5）
                    vh    viewpoint height，视窗高度，1vh等于视窗高度的1%
                    vw    viewpoint width，视窗宽度，1vw等于视窗宽度的1%

                2.使用scss，到插件市场安装  scss/sass编译  插件，然后就可以直接使用了，style支持scoped属性

				3.微信小程序自定义组件中只支持class选择器
      -->
      <view>
        <text>123</text>
      </view>
    </view>
  </view>
</template>
<script>
export default {
  data() {
    return {
      name: "cssScss",
    };
  },
  methods: {
    clickCssScss() {
      console.log("cssScss");
    },
  },
};
</script>
<style lang="scss" scoped>
#cssScss {
  font-size: 20px;
  text-align: center;
  line-height: 50px;
  color: darkcyan;
  text {
    color: red;
  }
}
</style>