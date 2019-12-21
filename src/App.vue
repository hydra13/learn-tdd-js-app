<template>
  <div>
    <NewMessageForm @send="addMessage" />
    <MessageList :messages="messages" />
  </div>
</template>

<script>
import NewMessageForm from "./components/NewMessageForm";
import MessageList from "./components/MessageList";
export default {
  name: "App",
  components: {
    NewMessageForm,
    MessageList
  },
  data() {
    return {
      messages: []
    };
  },
  methods: {
    addMessage(text) {
      this.messages.unshift(text);
    }
  }
};
</script>