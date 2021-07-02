<template>
  <div>
    <span v-if="seen">Now you see me</span>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class ConditionalsAndLoopsComponent extends Vue {
  seen: boolean = true;
}
</script>
