<template>
  <div>
    <h2 class="text-lg">{{ state.welcome }}</h2>
    <SimpleCounter />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { useOvermind } from "../overmind";
import SimpleCounter from "./SimpleCounter.vue";

export default defineComponent({
  name: "HelloWorld",
  components: {
    SimpleCounter,
  },
  setup() {
    const state = useOvermind.state();
    return { state };
  },
});
</script>
