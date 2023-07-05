<template>
  <h2>Todo List</h2>
  <button @click="getTodoList">Request Todo</button>
  <ul>
    <li v-for="todo in todoList" :key="todo.id">{{ todo.title }}</li>
  </ul>
  <p v-if="errorMessage">
    {{ errorMessage }}
  </p>
  <div>
    <label for="todo">할 일</label>
    <input type="text" v-model="todoItem.title" />
    <button @click="createTodo">전송 저장</button>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "TodoList",
  data() {
    return {
      todoList: [],
      errorMessage: "",
      todoItem: {
        title: "",
        completed: false,
      },
    };
  },
  methods: {
    getTodoList() {
      const url = "https://jsonplaceholder.typicode.com/todos";
      axios
        .get(url)
        .then((res) => (this.todoList = res.data))
        .catch((err) => {
          console.log(err);
          this.errorMessage = "에러가 발생";
        });
    },
    createTodo() {
      const url = "https://jsonplaceholder.typicode.com/todos";
      axios
        .post(url, this.todoItem)
        .then((res) => {
          console.log(res);
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>

<style>
.albumimage img {
  display: block;
  width: 300px;
  height: 300px;
}
.music {
  background: none;
}
.playlist {
  display: flex;
}
</style>
