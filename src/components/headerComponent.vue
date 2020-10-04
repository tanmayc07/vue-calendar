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

<style lang="scss" scoped>
h1 {
  margin-top: 20px;
  text-align: center;

  &:hover {
    cursor: pointer;
  }

  &::selection {
    color: lightblue;
    background-color: rgb(27, 27, 27);
  }
}
</style>
