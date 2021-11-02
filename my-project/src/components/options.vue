<template>
  <div class="color-options">
    
    <h1>Main Colors:</h1>
      <img v-for="mainColorImage in mainColors" :key="mainColorImage.image" v-bind:src="mainColors.image">
      <btn @click="myFunction()" class="main-color" v-for="mainColor in mainColors" :key="mainColor.name"> {{mainColor.name}} </btn>
    
    <h1>Secondary Colors:</h1>
      <btn class="secondary-color" v-for="secondaryColor in secondaryColors" :key="secondaryColor.name"> {{secondaryColor.name}} </btn>
    <h1>Accent Colors:</h1>
      <btn class="accent-color" v-for="accentColor in accentColors" :key="accentColor.name"> {{accentColor.name}} </btn>
    <h1>Chose A Wheel Type:</h1>
      <btn class="wheel-type" v-for="wheelType in wheelTypes" :key="wheelType.name"> {{wheelType.name}} </btn>
    <img style="display:none;" id="image" src="image">
  </div>
  </template>
  


<script>
export default {
  name: "Options",

  data() {
    return {
      mainColors: [
        {
          name: "Red",
          image: require("../assets/main/mainRed.png"),
        }, 
        {
          name: "Blue",
          image: require("../assets/main/mainBlue.png"),
        },
        {
          name: "Pink",
          image: require("../assets/main/mainPink.png"),
        },
        {
          name: "Orange",
          image: require("../assets/main/mainOrange.png"),
        },
        {
          name: "Green",
          image: require("../assets/main/mainGreen.png"),
        },
        {
          name: "Purple",
          image: require("../assets/main/mainPurple.png"),
        },
      ],

      secondaryColors: [
        {
          name: "Red",
          image: require("../assets/secondary/redSecondary.png"),
        },
        {
          name: "Blue",
          image: require("../assets/secondary/blueS.png"),
        },
        {
          name: "Pink",
          image: require("../assets/secondary/pinkS.png"),
        },
        {
          name: "Orange",
          image: require("../assets/secondary/orangeS.png"),
        },
        {
          name: "Green",
          image: require("../assets/secondary/greenS.png"),
        },
        {
          name: "Purple",
          image: require("../assets/secondary/purpleS.png"),
        },
      ],

      accentColors: [
        {
          name: "White",
          image: require("../assets/accent/whiteA.png"),
        },
        {
          name: "Black",
          image: require("../assets/accent/blackA.png"),
        },
        {
          name: "Grey",
          image: require("../assets/accent/greyA.png"),
        },
      ],

      wheelTypes: [
        {
          name: "Hard",
          image: require("../assets/wheels/wheelsHard.png"),
        },
        {
          name: "Intermediate",
          image: require("../assets/wheels/wheelsIntermediate.png"),
        },
        {
          name: "Medium",
          image: require("../assets/wheels/wheelsMedium.png"),
        },
        {
          name: "Soft",
          image: require("../assets/wheels/wheelsSoft.png"),
        },
        {
          name: "Wet",
          image: require("../assets/wheels/wheelsWet.png"),
        },
      ],
    };
   },

methods: {
  
myFunction: function () {	
		this.image = ""
}, 

}, 

  
</script>

<style>

.main-color {
  padding: 5px;
}

</style>