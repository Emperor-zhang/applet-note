<template>
  <view class="content">
    <view>{{ msg }}</view>
    <view :data-index="msg1">这里的属性是msg1</view>
    <view>------------循环遍历-----------------</view>
    <view v-for="item in list" :key="item.id">
      {{ item.text }}---{{ item.id }}
    </view>
    <view>-----------------------------</view>
    <!-- 需要一直显示隐藏切换的 使用v-if 不经常使用的就用v-show -->
    <view v-if="flag">v-if</view>
    <view v-else>v-else</view>
    <!-- <view v-show="flag">v-else</view> -->

    <view>{{ cnMoney }}</view>
    <view v-for="(item, index) in newList" :key="index">{{ item.text }} </view>
    <!-- <view v-for="(item1, index) in list1" :key="index">
      <view v-for="(item2, index) in list2" :key="index">
        {{ item1 }}*{{ item2 }}={{ item1 * item2 }}
      </view>
    </view> -->
    <view>--------------事件传参1---------------</view>
    <view data-index="111" @click="handleClick(1, $event)">点击</view>
    <com></com>
  </view>
</template>

<script>
import com from '../components/components'
export default {
  data() {
    return {
      flag: true,
      money: 1000,
      msg: '1.自动使用数据',
      msg1: '2.通过属性来使用标签',
      list: [
        {
          id: 0,
          text: '苹果',
        },
        {
          id: 1,
          text: '香蕉',
        },
        {
          id: 2,
          text: '葡萄',
        },
        {
          id: 4,
          text: '芒果',
        },
      ],
      list1: [1, 2, 3, 4, 5, 6, 7, 8, 9],
      list2: [1, 2, 3, 4, 5, 6, 7, 8, 9],
    }
  },
  methods: {
    handleClick(index, event) {
      console.log(index)
      console.log(event)
    },
  },
  components: {
    com,
  },
  // 计算属性
  computed: {
    // 把下面的cnMoney看成一个正常的属性 进行引用   不是一个方法
    cnMoney() {
      return '￥' + this.money
    },
    // 过滤出来list数组中id大于0的对象 newList 就是过滤后得到的新数组  然后进行展示
    newList() {
      return this.list.filter((v) => v.id > 0)
    },
  },
}
</script>

<style lang="scss"></style>
