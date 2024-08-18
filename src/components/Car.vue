<template>
  <Test />
  <h2>Coche</h2>
  <p>Marca {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>
    Color:
    <span v-for="(color, index) in colors" :key="index">
      {{ color + " " }}
    </span>
  </p>
  <p>Precio: {{ price }}</p>
  <p>
    Potencia Ciudad:
    <span v-for="(power, index) in powers" :key="index">
      <ul>
        <li v-if="power < 300">{{ power }}</li>
      </ul>
    </span>
  </p>

  <template v-for="(power, index) in powers" :key="index">
    <ul>
      <li v-if="power < 160"> Potencias Minimas: {{ power }}</li>
      <li v-else-if="power > 450"> Potencias maximas: {{ power }}</li>
      <li v-else>Potencias intermedias: {{ power }}</li>
    </ul>

  </template>
  <p>
    Potencia Carretera
    <ul v-for="(power, index) in powers" :key="index">
    <li v-if="power >= 300">{{ power }}</li>
  </ul>
  </p>
  <p>Mensaje {{ mensaje.text }}</p>
</template>

<script>
import Test from "./Test";
export default {
  // option api
  // data() {
  //   return {
  //     brand: "Audi",
  //     model: "A4",
  //     color: ["Azul", "Rojo", "Verde"],
  //     price: 38000,
  //     power: 180,
  //     mensaje: {
  //       title: "Hola Mundo",
  //       text: "Adios",
  //     },
  //   };
  // },
  setup() {
    const brand = "Audi";
    const model = "A4";
    const colors = ["Azul", "Rojo", "Morado", "Azul"];
    const price = 45000;
    const powers = [60, 80, 120, 160, 200, 280, 300, 390, 540, 500];
    const mensaje = {
      title: "Estoy Bien",
      text: "Welcome",
    };

    return {
      brand,
      model,
      colors,
      price,
      powers,
      mensaje,
    };
  },
  components: {
    Test,
  },
};
</script>

<style></style>
