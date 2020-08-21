<template>
  <view class="content">
    自定义组件
    <image class="img1" :src="mysrc" mode="widthFix"></image>
  </view>
</template>
<script>
export default {
  props: ['mysrc'],
}
</script>
<style>
.img1 {
  width: 100%;
  border-radius: 50%;
  border: 1px solid #ccc;
}
</style>
