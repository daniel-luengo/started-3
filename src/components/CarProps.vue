<template>
  <div>
    <h2>Car Props</h2>
    <p>Potencia {{ power }}</p>
  </div>
</template>

<script>
export default {
  props: {
    power: {
      type: String,
      default: 60,
    },
  },
  setup(props) {
    console.log(props.power);
  },
};
</script>

<style lang="scss" scoped></style>
