<template>
  <div
    id="character1"
    class="character"
    draggable="true"
    :ondragstart="dragStart">
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Character',
  setup() {
    return {};
  },
  methods: {
    dragStart: (event: any) => {
      event.dataTransfer.setData('id', event.target.id);
    },
  },
});
</script>

<style lang="scss" scoped>
  .character {
    border-radius: 50%;
    height: 35px;
    width: 35px;
    background-color: var(--accent);
  }
</style>
