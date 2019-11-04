<template>
  <div class="container">
    <div class="wrapper">
      <create-thread @new-thread="addThread" />
      <div v-for="thread in threads" :key="thread.id" class="thread-wrapper">
        <thread
          :title="thread.title"
          :username="thread.username"
          :content="thread.content"
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 16px;
  margin-top: 30px;
}
.thread-wrapper {
  padding: 10px;
}
.wrapper {
  max-width: 80%;
  margin: 0 auto;
}
</style>
<script>
import CreateThread from "./CreateThread";
import Thread from "./Thread";
export default {
  components: {
    Thread,
    CreateThread
  },
  data() {
    return {
      threads: [
        {
          id: 1,
          username: "Liliane",
          title: "consectetur omnis.",
          content:
            "Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis."
        },
        {
          id: 2,
          username: "Jerald",
          title: "Aut sequi molestiae quidem consectetur omnis.",
          content:
            "omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis."
        },
        {
          id: 3,
          username: "Jackson",
          title:
            "Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.",
          content:
            "Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis.Aut provident eligendi exercitationem exercitationem sequi molestiae quidem consectetur omnis."
        }
      ]
    };
  },
  methods: {
    addThread(thread) {
      this.threads.unshift(thread);
    }
  }
};
</script>
