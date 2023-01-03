<template>
  <div class="container">
    <div class="title">商品名称：{{title}}</div>
    <div class="price">价格：￥{{price}}</div>
    <div class="des">描述信息：{{des}}</div>
  </div>
</template>


<script>
//接收父组件传递过来的title属性，子组件进行渲染
export default {
  // 使用props接收的值，可以直接使用
  props: ['title', 'price', 'des']
}

/**
 * 传值总结：
 * 1、父组件给子组件传值，通过自定义属性传值
 * 2、子组件接受，使用props接受，接收到的值可以直接在子组件使用
 */
</script>

<style>
.container {
  width: 400px;
  height: 100px;
  border: 2px solid gray;
  margin: 20px;
  border-radius: 10px;
  padding: 20px;
}
</style>
