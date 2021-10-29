<template>
<div id="option">
<h2>
Chose A Main Color: {{ mainColors }}
</h2>
</div> 


  
</template>

<script>
export default {
  name: 'options',

  data() {
    return {
      mainColors: ['red', 'blue', 'orange', 'green', 'purple', 'pink'],    
      secondaryColors: ['red', 'blue', 'orange', 'green', 'purple', 'pink'], 
      accentColors: ['white', 'black', 'grey'], 
      wheelColors: ['blue', 'white', 'green', 'blue', 'yellow']
      }
  }
}
 
</script>