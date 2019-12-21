<template>
  <div>
    <input v-model="inputText" type="text" data-test="messageText" />
    <button @click="send" data-test="sendButton">Add message</button>
  </div>
</template>

<script>
export default {
  name: "NewMessageForm",
  data() {
    return {
      inputText: ""
    };
  },
  methods: {
    send() {
      this.$emit("send", this.inputText);
      this.inputText = "";
    }
  }
};
</script>