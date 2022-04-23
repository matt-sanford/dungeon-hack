<template>
  <div class="battlemat">
    <node
      v-for="(node, idx) in nodes"
      :key="idx"
      :node="node"
    />
  </div>
  <character/>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import Node from '@/types/node';
import node from '@/components/node.vue';
import character from '@/components/character.vue';

export default defineComponent({
  name: 'Battlemat',
  components: {
    node,
    character,
  },
  setup() {
    const nodeOne : Node = new Node('Stairs down');
    const nodeTwo : Node = new Node('Columns');
    const nodeThree : Node = new Node('Alter');
    const nodeRef : Array<Node> = [nodeOne, nodeTwo, nodeThree];
    const nodes = ref(nodeRef);

    return {
      nodes,
    };
  },
});
</script>

<style lang="scss" scoped>
  .battlemat {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
  }
</style>
