<template>
  <Header :text="text" />
</template>

<script>
import Header from "@/components/Header.vue";
export default {
  name: "App",
  components: {
    Header,
  },
  data() {
    return {
      text: "ini data text",
    };
  },
};
</script>

<style></style>
