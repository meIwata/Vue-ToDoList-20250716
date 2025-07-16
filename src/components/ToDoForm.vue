<template>
<!--  一個輸入表單用來新增代辦事項-->
<!--  label 提示要輸入什麼-->
<!--  input 是文字輸入框 會有id name屬性-->
<!--  按鈕用來新增代辦事項-->

  <form @submit.prevent="add">
    <label for="todo">新增代辦事項:</label>
    <input type="text" id="todo" name="todo" v-model="label" required />
    <button type="submit">新增</button>
  </form>
</template>

<script>
// 當按下新增按鈕時，會觸發onsubmit方法
// data 會有label和done兩個屬性用來儲存代辦事項
export default {
  name: 'ToDoForm',
  data() {
    return {
      label: ''
    };
  },
  methods: {
    // 當表單提交時，觸發add事件並傳遞輸入的值
    add() {
      const todoValue = this.label.trim();
      if (todoValue) {
        this.$emit('add', { label: todoValue, done: false });
        this.label = '';
      }
    }
  }
}

</script>


<style scoped>

</style>