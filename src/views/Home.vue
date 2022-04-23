<template>
  <div class="home">
    <battlemat />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import battlemat from '@/components/battlemat.vue';

export default defineComponent({
  name: 'Home',
  components: {
    battlemat,
  },
});
</script>
