<template>
  <view class="content">
    <image
      class="img"
      :src="mysrc"
      mode="widthFix"
      @click="handleClick"
    ></image>
  </view>
</template>
<script>
export default {
  props: ['mysrc'],
  methods: {
    handleClick() {
      this.$emit('func', this.mysrc)
    },
  },
}
</script>
<style>
.img {
  width: 100vw;
  border-radius: 50%;
  border: 1px solid #000;
}
</style>
