<template>
  <div class="chat-bot-app">
    <div class="chat-bot-app__header">
      <div class="chat-bot-app__header-title">
        <div class="chat-bot-app__header-title--name">IRIS</div>
        <div class="chat-bot-app__header-title--greet">
          <div class="chat-bot-app__header-title--greet-text">Hello</div>
          <img src="../assets/twemoji_waving-hand-light-skin-tone.svg" />
        </div>
        <div class="chat-bot-app__header-title--textintro">
          I am Iris, a Virtual Assistant
        </div>
        <div class="chat-bot-app__header-title--textdesc">
          How may I help you?
        </div>
      </div>
    </div>
    <div class="chat-bot-app__content">
      <div class="chat-bot-app__content__img">
        <div class="chat-bot-app__content__img-robot">
          <img src="../assets/Vector.svg" />
        </div>
      </div>
      <div class="chat-bot-app__content-ques">
        Frequently Asked Questions
        <img
          class="chat-bot-app__content-particular--bubble"
          src="../assets/Vector_question.svg"
        />
      </div>
      <div
        v-for="(header, index) in headers"
        :key="index"
        class="chat-bot-app__content-particular"
      >
        <img
          class="chat-bot-app__content-particular--bubble"
          src="../assets/Ellipse4.svg"
        />
        {{ header }}
      </div>
      <div class="chat-bot-app__content-submit">
        <img
          class="chat-bot-app__content-submit-msg"
          src="../assets/chat1.svg"
        />
        Start a New Conversation
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "chat-bot-app",
  data() {
    return {
      headers: [
        "Can i redeem my FB before the original term?",
        "How do I pay my Credit card bill?",
        "How can I get my Account Statement?",
        "What is the tenure of Fixed Deposit?",
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.chat-bot-app {
  width: 416px;
  height: 629px;
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: auto;
  border: 1px solid #e4e4e4;
  background: #ffffff;
  border-radius: 8px;
  box-shadow: 0px 0px 25px rgba(0, 0, 0, 0.05);
  &__header {
    // position: absolute;
    border-radius: 8px;
    width: 100%;
    background: linear-gradient(123.75deg, #f5821f 1.87%, #ff5c00 120.46%);
    &-title {
      width: 100%;
      &--name {
        display: flex;
        padding-left: 56px;
        padding-top: 20px;
        font-family: DM Sans;
        font-style: normal;
        font-weight: bold;
        font-size: 30px;
        line-height: 39px;
        /* identical to box height */
        color: #ffffff;
      }
      &--greet {
        display: flex;
        padding-left: 56px;
        font-family: DM Sans;
        font-style: normal;
        font-weight: bold;
        font-size: 22px;
        line-height: 29px;
        color: #ffffff;
        &-text {
          padding-right: 19px;
        }
      }
      &--textintro {
        display: flex;
        padding-left: 56px;
        font-family: DM Sans;
        font-style: normal;
        font-weight: 500;
        font-size: 18px;
        line-height: 23px;
        color: #ffffff;
      }
      &--textdesc {
        display: flex;
        padding-left: 56px;
        font-family: DM Sans;
        font-style: normal;
        font-weight: 500;
        font-size: 18px;
        line-height: 23px;
        /* or 128% */

        color: #ffffff;
        padding-bottom: 127px;
      }
    }
  }
  &__content {
    margin: -80px 13px 30px 13px;
    background: #ffffff;
    border: 1px solid #e4e4e4;
    box-sizing: border-box;
    box-shadow: 0px 0px 25px rgba(0, 0, 0, 0.05);
    border-radius: 8px;
    &__img {
      margin-left: 25px;
      margin-bottom: 17px;
      width: 67px;
      height: 67px;
      border-radius: 50%;
      background: linear-gradient(180deg, #ff7600 0%, #ff5c00 100%);
      box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.15);
      &-robot {
        margin-top: -30px;
        display: flex;
        align-items: center;
        justify-content: center;
        padding-top: 15px;
        border-radius: 100%;
      }
    }
    &-ques {
      display: flex;
      padding-left: 26px;
      font-family: DM Sans;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;
      color: #2d2d2d;
    }
    &-particular {
      display: flex;
      margin-left: 26px;
      margin-right: 26px;
      margin-top: 9px;
      padding-top: 15px;
      padding-bottom: 15px;
      background: #ffffff;
      border: 1px solid #e1e1e1;
      box-sizing: border-box;
      box-shadow: 0px 0px 8px rgba(0, 0, 0, 0.05);
      border-radius: 8px;
      font-family: DM Sans;
      font-style: normal;
      font-weight: normal;
      font-size: 12px;
      line-height: 21px;
      /* identical to box height, or 175% */

      color: #2d2d2d;
      &--bubble {
        margin-left: 8px;
        margin-right: 10px;
      }
    }
    &-submit {
      margin: 29px 61px 21px 61px;
      background: #ffffff;
      border: 1px solid #d1d1d1;
      box-sizing: border-box;
      box-shadow: 0px 4px 5px rgba(0, 0, 0, 0.1);
      border-radius: 100px;
      padding-top: 13px;
      padding-bottom: 13px;
      font-family: DM Sans;
      font-style: normal;
      font-weight: 500;
      font-size: 14px;
      line-height: 18px;

      color: #2d2d2d;
      &-msg {
        padding-right: 5px;
      }
    }
  }
}
</style>
