<template>
  <Test />
  <h2>Car Composition Api Vue3: Coche</h2>
  <p>Marca {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ powers }}</p>

  <button @click="upPower()">Aumentar</button>
  <button @click="downPower()">Disminuir</button>
  <!--  <p>
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
  <p>Mensaje {{ mensaje.text }}</p> -->
</template>

<script>
import Test from "./Test";
import { ref } from "vue";
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
    // const powers = [60, 80, 120, 160, 200, 280, 300, 390, 540, 500];
    let powers = ref(50);
    const mensaje = {
      title: "Estoy Bien",
      text: "Welcome",
    };

    //Las funciones van dentro de setup
    let upPower = () => {
      powers.value++;
      console.log(powers);
    };
    const downPower = () => {
      console.log("Disminuyendo potencia");
      powers.value--;
    };

    return {
      brand,
      model,
      colors,
      price,
      powers,
      mensaje,
      upPower,
      downPower,
    };
  },
  components: {
    Test,
  },
};
</script>

<style></style>
