<template>
  <div class="thread">
    <div class="thread-main">
      <h5 class="thread-user" v-text="username" />
      <h2 class="thread-title" v-text="title" />
      <p class="thread-content" v-text="content" />
    </div>
  </div>
</template>
<style scoped>
.thread {
  font-family: Arial, Helvetica, sans-serif;
  color: white;
  background-color: darkslategray;
  border-radius: 5px;
  border: 1px solid rgb(129, 131, 132);
  padding: 10px 25px;
}

.thread-title {
  font-size: 20px;
  padding-top: 10px;
  padding-bottom: 20px;
}
</style>
<script>
export default {
  props: {
    username: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    }
  }
};
</script>
