<template>
  <div class="calculator">
    <h2>Calculator Web</h2>
    <form name="calculator">
      <ul>
        <li>Angka 1 <input type="number" name="angka1" v-model="angka1"></li>
        <br />
        <li>Angka 2 <input type="number" name="angka2" v-model="angka2"></li>
        <br />
        <li>
          <button @click.prevent="tambah">+</button>
          <button @click.prevent="kurang">-</button>
          <button @click.prevent="bagi">/</button>
          <button @click.prevent="kali">x</button>
        </li>
        <br />
        <li>Hasil = <input type="number" name="hasil" v-model="hasil" readonly></li>
      </ul>
    </form>
  </div>
</template>


<script>
export default {
  data() {
    return {
      angka1: 0,
      angka2: 0,
      hasil: 0,
    };
  },
  methods: {
    tambah() {
      this.hasil = parseFloat(this.angka1) + parseFloat(this.angka2);
    },
    kurang() {
      this.hasil = parseFloat(this.angka1) - parseFloat(this.angka2);
    },
    bagi() {
      this.hasil = parseFloat(this.angka1) / parseFloat(this.angka2);
    },
    kali() {
      this.hasil = parseFloat(this.angka1) * parseFloat(this.angka2);
    },
  },
};
</script>

<style scoped>
.calculator {
  width: 200px;
  margin: 0 auto;
  text-align: center;
  font-family: Arial, sans-serif;
}

.calculator-display {
  margin-bottom: 10px;
  padding: 10px;
  background-color: #f4f4f4;
  border: 1px solid #ccc;
}

.calculator-buttons button {
  width: 45px;
  height: 45px;
  font-size: 20px;
  margin: 5px;
  cursor: pointer;
}
</style>
