<template>
<div id="option">
<h2>
 {{ mainColors }}
</h2>
</div> 


  
</template>

<script>
export default {
  name: 'options',

  data() {
    return {
    mainColors: [
      { 
        name: "Red", 
        image: require('../assets/main/mainRed.PNG') 
      }, 
      {
        name: "Blue", 
        image: require('../assets/main/mainBlue.PNG')
      }, 
      {
        name: "Pink", 
        image: require('../assets/main/mainPink.PNG')
      },
      { 
        name: "Orange", 
        image: require('../assets/main/mainOrange.PNG')
      },
      {
        mainColor: "Green", 
        image: require('../assets/main/mainGreen.PNG')
      },
      {
      mainColor: "Purple", 
        image: require('../assets/main/mainPurple.PNG')
      },
     ], 

    secondaryColors: [
      { 
        name: "Red", 
        image: require('../assets/secondary/secondaryRed.PNG') 
      }, 
      {
        name: "Blue", 
        image: require('../assets/secondary/secondaryBlue.PNG')
      }, 
      {
        name: "Pink", 
        image: require('../assets/secondary/secondaryPink.PNG')
      },
      { 
        name: "Orange", 
        image: require('../assets/secondary/secondaryOrange.PNG')
      },
      {
        mainColor: "Green", 
        image: require('../assets/secondary/secondaryGreen.PNG')
      },
      {
      mainColor: "Purple", 
        image: require('../assets/secondary/secondaryPurple.PNG')
      },
     ], 

    accentColors: [
      { 
        name: "White", 
        image: require('../assets/accent/accentWhite.PNG') 
      }, 
      {
        name: "Black", 
        image: require('../assets/accent/accentBlack.PNG')
      }, 
      {
        name: "Grey", 
        image: require('../assets/accent/accentGrey.PNG')
      },
     ], 

    wheelTypes: [
      { 
        name: "Hard", 
        image: require('../assets/wheels/wheelsHard.PNG') 
      }, 
      {
        name: "Intermediate", 
        image: require('../assets/wheels/wheelsIntermediate.PNG')
      }, 
      {
        name: "Medium", 
        image: require('../assets/wheels/wheelsMedium.PNG')
      },
      { 
        name: "Soft", 
        image: require('../assets/wheels/wheelsSoft.PNG')
      },
      {
        mainColor: "Wet", 
        image: require('../assets/wheels/wheelsWet.PNG')
      },
     ],     
    }
  }
}
</script>