<template>
  <div id="app">
    <h1>To-Do List</h1>
    <ToDoForm @add="handleAdd"></ToDoForm>
    <ul>
      <li v-for="(item, index) in todoItems" :key="index">
        <ToDoItem :label="item.label" :done="item.done"></ToDoItem>
      </li>
    </ul>
  </div>
</template>

<script>
// 使用todoitem.vue元件
// data新增todoitems 資料 裡面幫我新增四筆代辦事項
// 匯入 ToDoForm.vue 元件

import ToDoForm from './components/ToDoForm.vue';
import ToDoItem from './components/ToDoItem.vue';


export default {
  components: {
    ToDoForm,
    ToDoItem
  },
  data() {
    return {
      todoItems: [
        {label: '讀書', done: false},
        {label: '買便當', done: true},
        {label: '洗衣服', done: false},
        {label: '遛狗', done: true}
      ]
    };
  },
  methods: {
    handleAdd(newItem) {
      this.todoItems.push(newItem);
    }
  }
};
</script>


<!--<template>-->
<!--  <div id="app">-->
<!--    <h1>To-Do List</h1>-->
<!--    <ul>-->
<!--      <li>-->
<!--        <to-do-item label="my todo item1" :done="true"></to-do-item>-->
<!--      </li>-->
<!--      <li>-->
<!--        <to-do-item label="my todo item2" :done="false"></to-do-item>-->
<!--      </li>-->
<!--    </ul>-->
<!--  </div>-->

<!--</template>-->
<!--<script>-->
<!--import ToDoItem from "./components/ToDoItem.vue";-->

<!--export default {-->
<!--  name: "app",-->
<!--  components: {-->
<!--    ToDoItem,-->
<!--  },-->
<!--};-->
<!--</script-->
