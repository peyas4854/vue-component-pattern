<template>
  <div>
    <Navbar class="mb-3"></Navbar>
    <div class="container">

    <Home></Home>
    </div>
  </div>
</template>
<script>
import Home from "./View/Home.vue";
import Navbar from "./components/Nabvar.vue";

export default {
  name: "App",
  components: {
    Home,
    Navbar,
  },
};
</script>
