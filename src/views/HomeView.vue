<template>
  <div class="home">
    <h1>{{ title }}</h1>
    <input type="text" ref="name" />
    <button @click="handleClick">{{ title }}</button>
    <HelloWorld msg="Welcome to Your.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "HomeView",
  data() {
    return {
      title: "My First Vue app =D",
      count: 0,
    };
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name);
      this.$refs.name.classList.add("active");
      this.$refs.name.focus();
    },
  },
  components: {
    HelloWorld,
  },
};
</script>
