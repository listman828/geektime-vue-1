<template>
  <div id="app">
    {{msg}}
    <div>
      <input type="text" v-model="info">
      <button @click="handleClick">添加</button>
    </div>
    <ul>
      <TodoItem v-for="itemTest in list" :key="itemTest.id">
        <template v-slot:itemName="itemProps">
          <span :style="{fontSize: '20px',color:itemProps.checked?'red':'blue'}">{{itemTest}}</span>
        </template>
      </TodoItem>
    </ul>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import TodoItem from "./components/TodoItem.vue";

export default {
  name: "app",
  data() {
    return {
      msg: "hello geektime",
      info: "",
      list: []
    };
  },
  methods: {
    handleClick() {
      this.list.push(this.info);
      this.info = "";
    }
  },
  components: {
    HelloWorld,
    TodoItem
  }
};
</script>

<style>
</style>
