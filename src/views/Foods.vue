<template>
  <div>
    <NavBar />
    <h2>Food List</h2>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/Navbar.vue";

export default {
  name: "FoodList",
  components: {
    NavBar,
  },
};
</script>

<style></style>
