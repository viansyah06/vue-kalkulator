<template>
  <div id="app">
    <h1>Kalkulator Sederhana</h1>
    <Calculator />
  </div>
</template>

<script>
import Calculator from './components/Calculator-app.vue';

export default {
  components: {
    Calculator,
  },
};
</script>

<style>
#app {
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}

h1 {
  font-size: 2em;
}

</style>
