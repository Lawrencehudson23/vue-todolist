<template>
  <div id="app">
    <Header />
    <AddTodo />
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Header from "./components/layout/Header";
import Todos from "./components/Todos";
import AddTodo from "./components/AddTodo";
export default {
  name: "app",
  components: { Header, Todos, AddTodo },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "todo 1",
          completed: false,
        },
        {
          id: 2,
          title: "todo 2",
          completed: true,
        },
        {
          id: 3,
          title: "todo 3",
          completed: false,
        },
      ],
    };
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter((todo) => todo.id !== id);
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
.btn {
  display: inline-block;
  bottom: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}
.btn:hover {
  background: #666;
}
</style>
