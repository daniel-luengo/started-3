<template>
  <h1>Vue js</h1>
  <CarProps :power="power" />
</template>

<script>
import CarProps from "./components/CarProps.vue";
export default {
  components: {
    CarProps,
  },
  setup() {
    let power = 30;

    return {
      power,
    };
  },
};
</script>

<style></style>
