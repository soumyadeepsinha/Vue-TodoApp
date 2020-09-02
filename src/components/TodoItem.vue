<template>
  <div class="todo_item" v-bind:class="{'is_complete':todo.completed}">
    <input type="checkbox" v-on:change="markComplete" />
    <p>
      {{todo.title}}
      <button class="del" @click="$emit('del-todo', todo.id)">x</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    },
  },
};
</script>
local
<style scoped>
.todo_item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px dotted #ccc;
}

.is_complete {
  text-decoration: line-through;
}

.del {
  background: #ff0000;
  color: #fff;
  border: none;
  padding: 5px 10px;
  border-radius: 50%;
  cursor: pointer;
  float: right;
}
</style>