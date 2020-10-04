<template>
  <h1>Calendar By {{ name }}</h1>
</template>

<script>
export default {
  setup() {
    const name = "Tanmay";

    return {
      name,
    };
  },
};
</script>

<style scoped>
h1 {
  text-align: center;
}
</style>