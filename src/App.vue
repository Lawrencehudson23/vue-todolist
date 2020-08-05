<template>
  <div id="app">
    <Todos v-bind:todos="todos" />
  </div>
</template>

<script>
import Todos from "./components/Todos";
export default {
  name: "app",
  components: { Todos },
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
</style>
