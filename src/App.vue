<template>
  <div class="container">
    <h1 class="pageTitle">Date Picker</h1>
    <date-picker></date-picker>
    <p> test </p>
  </div>
</template>

<script>
// import { ref, onMounted } from 'vue';

import DatePicker from '@/components/DatePicker';

export default {
  name: 'App',
  components: {
    DatePicker,
  },
  setup() {
    const months = [
      'January',
      'February',
      'March',
      'April',
      'May',
      'June',
      'July',
      'August',
      'September',
      'October',
      'November',
      'December',
    ];

    const startingYear = 2010;
    const numberofYears = 20;

    return {
      months,
      numberofYears,
      startingYear,
    };
  },
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
