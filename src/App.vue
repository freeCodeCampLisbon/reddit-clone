<template>
  <div id="app">
    <toolbar />
    <thread-container />
  </div>
</template>
<script>
import Toolbar from "./components/Toolbar";
import ThreadContainer from "./components/ThreadContainer";
export default {
  name: "app",
  components: {
    Toolbar,
    ThreadContainer
  }
};
</script>

<style></style>
