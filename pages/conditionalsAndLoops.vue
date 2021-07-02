<template>
  <div>
    <span v-if="seen">Now you see me</span>
    <div>
      <ol>
        <li v-for="list in lists" v-bind:key="list.key">
          {{ list.value }}
        </li>
      </ol>
    </div>
    <TopLink />
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

interface List {
  key: string;
  value: string;
}

@Component
export default class ConditionalsAndLoopsComponent extends Vue {
  private seen: boolean = true;
  private lists: List[] = [
    {
      key: "1",
      value: "Learn JavaScript",
    },
    {
      key: "2",
      value: "Learn Vue",
    },
    {
      key: "3",
      value: "Build something awesome",
    },
  ];
}
</script>
