<template>
  <view class="content">
    <com :mysrc="src1"></com>
    <com :mysrc="src2"></com>
  </view>
</template>

<script>
import com from '../components/components'
export default {
  data() {
    return {
      src1:
        'https://ss3.bdstatic.com/70cFv8Sh_Q1YnxGkpoWK1HF6hhy/it/u=189046959,2449680816&fm=26&gp=0.jpg',
      src2:
        'https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=1774633864,2097153823&fm=26&gp=0.jpg',
    }
  },
  components: {
    com,
  },
}
</script>

<style lang="scss"></style>
