<template>
  <div class="inputBox">
    <input type="text" v-model="inputText" @keyup.enter="keyEntered">
  </div>
</template>
<script>
export default {
  data() {
    return {
      inputText: ""
    };
  },
  methods: {
    keyEntered() {
      this.$emit("add-note", {
        note: this.inputText,
        timestamp:
          new Date().toLocaleDateString() +
          " " +
          new Date().toLocaleTimeString()
      });
      this.inputText = "";
    }
  }
};
</script>
<style>
.inputBox {
  text-align: center;
  margin-bottom: 15px;
}
</style>