<template>
  <chat-bot-page />
</template>

<script>
import chatBotPage from "./components/chatBotPage.vue";

export default {
  name: "App",
  components: {
    chatBotPage,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
