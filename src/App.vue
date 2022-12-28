<template>
  <div class="container mx-auto">
    <p>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </p>
    <router-view></router-view>
  </div>
  <!-- <div class="container mx-auto">
    <h2 class="text-red-700 font-bold">{{ msg }}</h2>
    <div
      v-for="course in courses"
      :key="course.id"
      class="shadow p-4 mb-4 border border-gray-200"
    >
      <h2>{{ course.name }}</h2>
      <p>{{ course.description }}</p>
    </div>
    <button class="bg-blue-500 text-white font-semibold py-2 px-4 rounded-lg">
      Test
    </button>
  </div> -->
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      msg: "Allah Mohan",
      courses: [
        {
          id: 1,
          name: "Laravel",
          description:
            "Lorem ipsum dolor sit amet consectetur adipiscing elit nulla, fusce venenatis porttitor ridiculus libero aenean.",
          price: 100,
        },
        {
          id: 2,
          name: "PHP",
          description:
            "Lorem ipsum dolor sit amet consectetur adipiscing elit nulla, fusce venenatis porttitor ridiculus libero aenean.",
          price: 500,
        },
        {
          id: 3,
          name: "JavaScript",
          description:
            "Lorem ipsum dolor sit amet consectetur adipiscing elit nulla, fusce venenatis porttitor ridiculus libero aenean.",
          price: 900,
        },
      ],
    };
  },
  mounted() {
    this.test();
  },
  methods: {
    test() {
      this.msg = "This is our Name";
    },
  },
};
</script>
