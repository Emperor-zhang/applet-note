<template>
  <view class="content">
    <com @func="handleSrc" :mysrc="src1"></com>
    <view>-----------------trtretr-----------------</view>
    <com @func="handleSrc" :mysrc="src2"></com>
  </view>
</template>

<script>
import com from '@/pages/components/imgborder.vue'
export default {
  data() {
    return {
      src1:
        'https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=189046959,2449680816&fm=26&gp=0.jpg',
      src2:
        'https://ss0.bdstatic.com/70cFvHSh_Q1YnxGkpoWK1HF6hhy/it/u=3929115075,3008788471&fm=26&gp=0.jpg',
    }
  },
  components: {
    com,
  },
  mounted() {
    console.log(this.baseUrl)
  },
  methods: {
    handleSrc(data) {
      console.log(data)
    },
    onLoad() {
      console.log(this.baseUrl)
      console.log(getApp().globalData.base)
    },
  },
}
</script>

<style lang="scss"></style>
