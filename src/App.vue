<template>
  <header-component />
  <calendar-component />
</template>

<script>
import headerComponent from "./components/headerComponent";
import calendarComponent from "./components/calendarComponent";

export default {
  setup() {
    return {
      "header-component": headerComponent,
      "calendar-component": calendarComponent,
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Noto+Serif+SC:wght@400;500&display=swap");

* {
  font-family: "Noto Serif SC", serif;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>
