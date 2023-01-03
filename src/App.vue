<template>
  <div>
    <!--3、使用helloWorld组件-->
    <HelloWorld
      v-for="item in list"
      :key="item.id"
      :title="item.proname"
      :price="item.proprice"
      :des="item.id"
      @parentKan="a"
    />
  </div>
</template>

<script>
/**
 * 父传子传值总结：
 * 1、父组件给子组件传值，通过自定义属性传值
 * 2、子组件接受，使用props接受，接收到的值可以直接在子组件使用
 */

/**
 * 1、父组件定义methods方法
 * 2、父亲通过自定义事件传递给子组件 <hello-world @事件名="事件处理函数"></hello-world>
 * 3、儿子组件通过this.$emit('事件名') 触发父亲传递过来的自定义事件
 */
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  // 2、注册hello-world组件
  components: {
    HelloWorld
  },
  data() {
    return {
      // 模拟从后端拿到数据
      list: [
        {id: 1, proname: '超级好吃的棒棒糖', proprice: 18.8},
        {id: 2, proname: '超级好吃的大鸡腿', proprice: 34.2},
        {id: 3, proname: '超级无敌的冰激凌', proprice: 14.2}
      ]
    }
  },
  methods: {
    // 父组件提供了一个用于修改价格的方法
    a() {
      console.log('砍价')
    }
  },
}
</script>
