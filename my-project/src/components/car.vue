<template>
<div class="car-box">
  <img src="../assets/car.png" alt="car image" class="car-image">
</div>
</template>

<script>
export default {
  name: 'car',
  props: {
    msg: String
  }
}
</script>

<style>

.car-box {
 margin-top: 70px;
 padding: -20px;
}

.car-image {
  max-width: 700px;  
  max-height: 700px;
}

</style>

