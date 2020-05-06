<template>
  <div>
    <!-- <span>{{message}}</span>
    <todo-item :auth="write.title"></todo-item> -->
    <p>父组件数值：{{num}}</p>
    <button @click="addNum">按钮</button>
    <todo-item @addParentNum="acceptNum" :cnum="num"></todo-item>
    <p>父组件接受子组件发来的值：{{pnum}}</p>
  </div>
</template>

<script>
import TodoItem from "./TodoItem.vue";
export default {
  data() {
    return {
      message: "I am a parent",
      write: {
        title: "parent to chidren"
      },
      num: 0,
      pnum: 7
    };
  },
  components: {
    TodoItem
  },
  methods: {
    addNum() {
      this.num = this.num + 1;
    },
    acceptNum(e){
      console.log(this.pnum);
      this.pnum = e;
    }
  }
};
</script>

<style scoped>
</style>
