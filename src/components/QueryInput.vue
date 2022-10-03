<script>
import { ref } from 'vue';
export default {
  setup() {
    const query = ref('');

    const reset = () => {
      query.value = ''; // clear query
    };
    return {
      reset,
      query,
    };
  },
};
</script>

<template>
  <h2>Query input</h2>
  <div class="flex">
    <input type="text" placeholder="Filter Search" v-model="query" />
    <p>{{ query }}</p>
    <button @click="reset">Clear</button>
  </div>
</template>

<style lang="css" scoped>
.flex {
  display: flex;
  gap: 12px;
}
</style>
