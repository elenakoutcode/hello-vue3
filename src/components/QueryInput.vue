<template>
  <div>
    <h2>Query input</h2>
    <input type="text" placeholder="Filter Search" v-model="query" />
    <p>{{ query }}</p>
    <button @click="reset">Clear</button>
  </div>
</template>

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
      query
    };
  }
};
</script>
