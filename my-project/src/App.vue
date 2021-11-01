<template>
  <div id="app">
    <div class="header">
      <div class="title">
        <h1>DESIGN YOUR OWN F1 CAR</h1>
      </div>
      <car />
      <Options />
    </div>
  </div>
</template>

<script>
import car from "./components/car.vue";
import Options from "./components/Options.vue";

export default {
  name: "App",
  components: {
    car,
    Options,
  },
};
</script>
  

<style>
body {
  background-color: rgb(247, 237, 225);
}

.header {
  display: flex;
  justify-content: center;
  align-content: center;
  padding: 30px;
  margin-top: 20px;
}
.title {
  font-size: 20px;
  letter-spacing: 3px;
}
</style>
