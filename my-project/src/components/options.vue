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
      colors: [
        {
        mainColor: "Red", 
        image: require('../assets/main/mainred.PNG'), 
        mainColor: "Blue", 
        image: require('../assets/main/mainblue.PNG'), 
        mainColor: "Pink", 
        image: require('../assets/main/mainpink.PNG'),
        mainColor: "Orange", 
        image: require('../assets/main/mainorange.PNG'),
        mainColor: "Green", 
        image: require('../assets/main/maingreen.PNG'),
        mainColor: "Purple", 
        image: require('../assets/main/mainpurple.PNG'),
        },

        {
        secondaryColor: "Red", 
        image: require('../assets/main/mainred.PNG'), 
        secondaryColor: "Blue", 
        image: require('../assets/main/mainblue.PNG'), 
        secondaryColor: "Pink", 
        image: require('../assets/main/mainpink.PNG'),
        secondaryColor: "Orange", 
        image: require('../assets/main/mainorange.PNG'),
        secondaryColor: "Green", 
        image: require('../assets/main/maingreen.PNG'),
        secondaryColor: "Purple", 
        image: require('../assets/main/mainpurple.PNG'),
        }

     ]

    

  }
     
  }
 
</script>