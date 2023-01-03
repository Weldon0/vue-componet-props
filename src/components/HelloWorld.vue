<template>
  <div class="container">
    <div class="title">商品名称：{{ title }}</div>
    <div class="price">价格：￥{{ price }}</div>
    <div class="des">描述信息：{{ des }}</div>
    <button @click="kan">砍价-10元</button>
  </div>
</template>


<script>
//接收父组件传递过来的title属性，子组件进行渲染

// 如果子组件要修改父组件传递过来的数据，子组件不能直接修改
// 可以通过触发父组件的自定义方法，让父组件自己修改
export default {
  // 使用props接收的值，可以直接使用
  props: ['title', 'price', 'des'],
  methods: {
    kan() {
      // // 从props接收过来的数据，子组件不能直接修改
      // // 直接修改会报错
      // console.log(this.price)
      // // 需求：price减少十元
      // this.price = this.price - 10

    //   直接触发
      this.$emit('parentKan')
    }
  },
}


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
