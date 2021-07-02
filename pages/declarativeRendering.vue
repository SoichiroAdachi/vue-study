<template>
  <div>
    <div>Message: {{ message }}</div>
    <Nuxt-link to="/"> 戻る </Nuxt-link>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class TestComponent extends Vue {
  message: string = "This is a message";
}
</script>