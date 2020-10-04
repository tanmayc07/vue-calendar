<template>
  <div id="calendar__container">
    <div class="calendar__header">
      <h2>{{ month }}</h2>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const month = ref("January 2020");

    return {
      month,
    };
  },
};
</script>

<style lang="scss" scoped>
#calendar__container {
  width: 80%;
  height: 46em;
  margin: 5em auto;
  background-color: rgb(235, 235, 235);
  border: 1px solid grey;
  border-radius: 15px;

  .calendar__header {
    text-align: center;
    color: rgb(3, 3, 3);
    background-color: rgb(195, 195, 195);
    width: 100%;
    height: 4em;
    margin: 0 auto;
    padding: 10px;
    border-bottom: 1px solid grey;
    border-radius: 15px;
  }
}
</style>
