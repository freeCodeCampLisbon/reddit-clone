<template>
  <div class="navbar">
    <h2 class="nav-title">Reddit Clone</h2>
    <ul class="nav-links">
      <li>Home</li>
      <li>About</li>
    </ul>
  </div>
</template>
<style scoped>
.navbar {
  color: white;
  padding: 5px 15px;
  background-color: red !important;
  display: flex;
  height: 64px;
  align-items: center;
  justify-content: space-between;
}
.nav-links {
  list-style-type: none;
  display: flex;
  margin-right: -10px;
  margin-left: -10px;
}
.nav-links li {
  padding: 0px 10px;
}
</style>
<script>
export default {};
</script>
