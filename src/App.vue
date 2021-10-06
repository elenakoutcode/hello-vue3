<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <query-input></query-input>
</template>

<script>
import QueryInput from './components/QueryInput.vue';
export default {
  name: 'App',
  components: {
    QueryInput
  }
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');

*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  /* Variables Decleration */
  --main-font: 'Source Sans Pro', sans-serif;
}

html {
  font-family: 'Roboto', sans-serif;
  font-size: 10px;
  color: #1e1e1e;
}

.container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.pageTitle {
  padding: 20px 40px;
  margin-bottom: 42px;
  background-color: rgb(54, 54, 161);
  color: #f1f1f1;
}
</style>
