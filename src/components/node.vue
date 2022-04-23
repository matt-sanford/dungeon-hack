<template>
  <article class="node">
    <h2>{{node.name}}</h2>
    <div
      class="node-drop"
      :ondrop="drop"
      :ondragover="dragOver"
    ></div>
  </article>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Node from '@/types/node';

export default defineComponent({
  name: 'Node',
  props: {
    node: Node,
  },
  methods: {
    drop(event: any) {
      event.preventDefault();
      const id = event.dataTransfer.getData('id');
      event.target.appendChild(document.getElementById(id));
    },
    dragOver(event: any) {
      event.preventDefault();
    },
  },
});
</script>

<style lang="scss" scoped>
  .node {
    background-color: var(--dark);
    border-radius: 5px;
    margin: 10px;
    padding: 5px;
    min-width: 100px;

    h2 {
      color: var(--font);
      padding: 3px;
    }

    .node-drop {
      display: flex;
      align-items: center;
      justify-content: space-around;
      flex-wrap: wrap;
      margin: 3px;
      border: 2px dotted var(--font);
      border-radius: 5px;
      min-height: 20px;
      padding: 3px;
    }
  }
</style>
