<template>
  <div>
    <div>Message: {{ message }}</div>
    <TopLink />
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class DeclarativeRendering extends Vue {
  private message: string = "This is a message";
}
</script>