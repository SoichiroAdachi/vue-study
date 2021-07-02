<template>
  <div>
    <p
      class="mt-4 pt-4 text-gray-800 border-t border-dashed"
      v-for="pageInfo in pageInfoList"
      v-bind:key="pageInfo.key"
    >
      <Nuxt-link :to="pageInfo.pageName">{{ pageInfo.title }}</Nuxt-link>
    </p>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

interface PageInfo {
  key: string;
  pageName: string;
  title: string;
}

@Component
export default class TutorialComponent extends Vue {
  private pageInfoList: PageInfo[] = [
    {
      key: "1",
      pageName: "/declarativeRendering",
      title: "宣言的レンダリング",
    },
    {
      key: "2",
      pageName: "/conditionalsAndLoops",
      title: "条件分岐とループ",
    },
    {
      key: "3",
      pageName: "/handlingUserInput",
      title: "ユーザー入力の制御",
    },
  ];
}
</script>