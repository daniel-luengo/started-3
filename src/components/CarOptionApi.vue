<template>
  <h2>Coche - Option API</h2>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>

  <button @click="upPower">Aumentar</button>
  <button @click="downPower">Disminuir</button>
</template>

<script>
export default {
  data() {
    return {
      brand: "Seat",
      model: "Leon",
      power: 50,
    };
  },
  methods: {
    upPower() {
      console.log("Aumentando potencia => ");
      this.power = this.power + 1;
    },
    downPower() {
      console.log("Bajando potencia");
      this.power = this.power - 1;
    },
  },
};
</script>

<style lang="scss" scoped></style>
