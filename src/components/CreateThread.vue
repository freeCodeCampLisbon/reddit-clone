<template>
  <form @submit.prevent="onFormCreate" class="new-thread">
    <div class="form-row">
      <div class="form-item">
        <label>
          Username:
        </label>
        <input
          required
          class="input"
          type="text"
          placeholder="username"
          v-model="username"
        />
      </div>
    </div>
    <div class="form-row">
      <div class="form-item">
        <label>
          Thread title:
        </label>
        <input
          required
          class="input"
          type="text"
          placeholder="title"
          v-model="title"
        />
      </div>
    </div>
    <div class="form-row">
      <div class="form-item">
        <label>
          Thread title:
        </label>
        <textarea
          cols="20"
          rows="50"
          class="input textarea"
          placeholder="content"
          required
          v-model="content"
        ></textarea>
      </div>
    </div>
    <div class="form-row">
      <button :disabled="!isValid">Create Thread</button>
    </div>
  </form>
</template>
<style scoped>
.new-thread {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
label {
  display: block;
  margin-bottom: 5px;
}
.form-row {
  flex: 1;
  width: 90%;
  padding: 10px 0px;
}
.textarea {
  resize: none;
  min-height: 200px;
}
.input {
  padding: 0px 5px;
  height: 20px;
  width: 100%;
}
button {
  height: 30px;
  width: 150px;
  display: block;
  margin: 0 auto;
  background: black;
  color: white;
  transition: 0.3s ease-in-out;
}

button:disabled {
  opacity: 0.3;
}
</style>
<script>
export default {
  data() {
    return {
      title: "",
      content: "",
      username: ""
    };
  },
  computed: {
    isValid() {
      return this.title && this.username && this.content;
    }
  },
  methods: {
    onFormCreate() {
      this.$emit("new-thread", {
        title: this.title,
        content: this.content,
        username: this.username
      });
      this.title = "";
      this.content = "";
      this.username = "";
    }
  }
};
</script>
