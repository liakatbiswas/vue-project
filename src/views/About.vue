<template>
  <div class="flex flex-wrap mx-4">
    <div v-for="todo in todos" :key="todo.id" class="w-1/3 px-4 mt-6">
      <div
        class="border border-gray-200 bg-gray-300 rounded-lg hover:bg-red-500 hover:text-white p-6 h-full"
      >
        <p>{{ todo.id }}</p>
        <h2 class="font-bold mb-2 text-lg">{{ todo.title }}</h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      todos: [],
    };
  },
  mounted() {
    fetch("https://jsonplaceholder.typicode.com/todos")
      .then((response) => response.json())
      .then((json) => (this.todos = json));
  },
};
</script>
