<template>
  <div id="app">
    <div class="header">
      <div class="title">
        <h1>DESIGN YOUR OWN F1 CAR</h1>
      </div>
      <options />
    </div>
  </div>
</template>

<script>
import options from "./components/options.vue";

export default {
  name: "App",
  components: {
    options,
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
