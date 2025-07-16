<script>
import { defineComponent } from 'vue';

export default defineComponent({
  props: {
    label: {
      type: String,
      required: true
    },
    done: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      isDone: this.done,
      id: crypto.randomUUID()
    };
  }
});
</script>

<template>
  <div>
    <input
      type="checkbox"
      :id="id"
      v-model="isDone"
      :checked="isDone"
    />
    <label :for="id">{{ label }}</label>
  </div>
</template>

<style scoped>

</style>







<!--<script>-->
<!--export default {-->
<!--  props: {-->
<!--    label: {required: true, type: String},-->
<!--    done: {default: false, type: Boolean}-->
<!--  },-->
<!--  data() {-->
<!--    return {-->
<!--      isDone: this.done,-->
<!--      id: "todo-" + crypto.randomUUID(),-->
<!--    };-->
<!--  },-->
<!--};-->
<!--</script>-->

<!--<template>-->
<!--  <div>-->
<!--    &lt;!&ndash;    <input type="checkbox" id="todo-item" v-bind:checked="isDone" />&ndash;&gt;-->
<!--    <input type="checkbox" v-bind:id="id" :checked="isDone"/> &lt;!&ndash; v-bind去除也可以 &ndash;&gt;-->

<!--    <label v-bind:for="id">{{ label }}</label>-->
<!--  </div>-->
<!--</template>-->

<!--<style scoped>-->

<!--</style>-->