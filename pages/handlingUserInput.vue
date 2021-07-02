<template>
  <div>
    <p>{{ message }}</p>
    <button v-on:click="reverseMessage">Reverse Message</button>
    <div><TopLink /></div>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class HandlingUserInput extends Vue {
  private message: string = "Hello Vue.js!";

  reverseMessage() {
    this.message = this.message.split("").reverse().join("");
  }
}
</script>
