<script>
export default {
  onLaunch: function () {
    console.log('App Launch')
  },
  onShow: function () {
    console.log('App Show')
  },
  onHide: function () {
    console.log('App Hide')
  },
  mounted () {
    console.log("mounted")
  },
  created () {
    console.log("created")
  },
  globalData: {
    base: '链接地址',
  },
}
</script>

<style>
/*每个页面公共css */
</style>
