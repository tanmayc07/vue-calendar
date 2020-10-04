<template>
  <div id="calendar__container">
    <div class="calendar__header">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="icon icon-tabler icon-tabler-arrow-left-circle left-arrow"
        width="44"
        height="44"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <circle cx="12" cy="12" r="9" />
        <line x1="8" y1="12" x2="16" y2="12" />
        <line x1="8" y1="12" x2="12" y2="16" />
        <line x1="8" y1="12" x2="12" y2="8" />
      </svg>
      <h2>{{ month }}</h2>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="icon icon-tabler icon-tabler-arrow-right-circle right-arrow"
        width="44"
        height="44"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        fill="none"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <circle cx="12" cy="12" r="9" />
        <line x1="16" y1="12" x2="8" y2="12" />
        <line x1="16" y1="12" x2="12" y2="16" />
        <line x1="16" y1="12" x2="12" y2="8" />
      </svg>
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
    color: rgb(0, 0, 0);
    background-color: rgb(195, 195, 195);
    width: 100%;
    height: 4em;
    margin: 0 auto;
    padding: 10px;
    border-bottom: 1px solid grey;
    border-radius: 15px;
    display: grid;
    grid-template-rows: 25% 50% 25%;
    grid-template-areas: "left center right";

    .left-arrow {
      grid-area: left;
    }

    .right-arrow {
      grid-area: right;
      justify-self: end;
    }

    svg {
      &:hover {
        cursor: pointer;
        color: white;
        opacity: 0.7;
      }
    }

    h2 {
      grid-area: center;
      justify-self: center;

      &::selection {
        color: lightblue;
      }

      &:hover {
        color: rgb(251, 251, 251);
        cursor: pointer;
      }
    }
  }
}
</style>
