<template>
  <div class="date-picker">
    <div class="custom-select">
      <select>
        <option v-for="(month, index) in months" :key="month" :value="index">
          {{ month }}
        </option>
      </select>
    </div>
    <div class="custom-select">
      <select>
        <option
          v-for="i in numberofYears"
          :key="i"
          :value="startingYear + (i - 1)"
        >
          {{ startingYear + (i - 1) }}
        </option>
      </select>
    </div>
  </div>
</template>

<script>
// import { ref, onMounted } from 'vue';

export default {
  name: 'DatePicker',
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

<style scoped>
/* wrapper-div for including arrow */
.custom-select {
  background-color: #eee;
  float: left;
  margin-right: 10px;
  position: relative;
}

.custom-select select {
  -moz-appearance: none;
  -webkit-appearance: none;
  appearance: none; /* remove default styling */
  background-color: inherit;
  border: none;
  color: #333;
  display: block;
  font-size: 16px;
  height: 32px;
  padding: 5px 30px 5px 10px;
  margin: 0;
  outline: none;
}

/* drop arrow */
.custom-select:after {
  content: '\25bc';
  color: #aaa;
  font-size: 12px;
  position: absolute;
  right: 8px;
  top: 10px;
}
</style>