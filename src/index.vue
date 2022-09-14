<script setup>
  defineProps({
    goodsImg: {
      type: String,
      required: true,
    },
    goodsName: {
      type: String,
      required: true,
    },
    goodsDescribe: {
      type: String,
      required: true,
    },
    goodsPrice: {
      type: String || Number,
      required: true,
    },
    link: {
      type: String,
      default: '',
    },
  });


  </script>

<template>
  <a
    :href="link"
    class="goods-card"
  >
    <div class="goods-img">
      <img :src="goodsImg" alt="">
    </div>
    <div class="goods-info">
      <div>{{ goodsName }}</div>
      <div>{{ goodsDescribe }}</div>
      <div>￥{{ goodsPrice }}</div>
    </div>
  </a>

</template>

<style lang="scss" scoped>
.goods-card {
width: 100%;
height: 100%;
display: block;

.goods-img {
  width: 100%;
  // 计算盒子的三分之二的高度
  height: calc(100% * 2 / 3);
  overflow: hidden;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}

.goods-info {
  width: 100%;
  // 计算盒子的三分之一的高度
  height: calc(100% * 1 / 3);
  text-align: center;

  div {
    /* 第一步：让文字强制一行显示 */
    white-space: nowrap;
    /* 第二步：溢出隐藏 */
    overflow: hidden;
    /* 第三步：溢出的内容省略号显示 */
    text-overflow: ellipsis;
    // 计算盒子的三分之一的上内边距
    padding-top: calc(100% * 1 / 3 / 6);
    color: black;

    &:nth-child(2) {
      color: #999;
    }

    &:nth-child(3) {
      color: #cf4444;
      font-size: 20px;
    }
  }
}
}
</style>
