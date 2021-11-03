<template>
  <div class="color">

  <div class="color-options">
  <h1>Main Colors:</h1>
  <ul>
    <li 
    class="main-color" 
    v-for="(mainColor, position) in possibleMainColors" 
    :key="position" v-on:click="addMainImage"> {{mainColor.name}} 
    </li>
   </ul>

   <h1>Secondary Colors:</h1>
  <ul>
    <li 
    class="secondary-color" 
    v-for="(secondaryColor, position) in possibleSecondaryColors" 
    :key="position" v-on:click="addSecondaryImage"> {{secondaryColor.name}} 
    </li>
  </ul>

  <h1>Accent Colors:</h1>
  <ul>
    <li 
    class="accent-color" 
    v-for="(accentColor, position) in possibleAccentColors" 
    :key="position" v-on:click="addAccentImage"> {{accentColor.name}} 
    </li>
   </ul>

  <h1>Chose A Wheel Type:</h1>
  <ul>
    <li 
    class="wheel-type" 
    v-for="(wheelType, position) in possibleWheelTypes" 
    :key="position" v-on:click="addWheelImage"> {{wheelType.name}} 
    </li>
   </ul>
  </div>

  <div class="color-image">
  <ul>
    <div class="main-image" v-for="(mainColor, position) in mainColors" :key="position">
    <img :src="mainColor.image" alt="" />
    </div>
  </ul>
  <ul>
    <div class="secondary-image" v-for="(secondaryColor, position) in secondaryColors" :key="position">
    <img :src="secondaryColor.image" alt="" />
    </div>
  </ul>
  <ul>
    <div class="accent-image" v-for="(accentColor, position) in accentColors" :key="position">
    <img :src="accentColor.image" alt="" />
    </div>
  </ul>
  <ul>
    <div class="wheel-image" v-for="(wheelType, position) in wheelTypes" :key="position">
    <img :src="wheelType.image" alt="" />
    </div>
  </ul>
  </div>
   
  </div>
  </template>
  


<script>
export default {
  name: "Options",

  data() {
    return {
      mainColors: [],
      possibleMainColors: [
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

      secondaryColors: [], 
      possibleSecondaryColors: [
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

      accentColors: [], 
      possibleAccentColors: [
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

      wheelTypes: [],
      possibleWheelTypes: [
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
    addMainImage: function (event) {
    const img = event.target.innerText;
    const found = this.possibleMainColors.filter((el) => el.name === img);
    this.mainColors.push(found[0]);
    },

    addSecondaryImage: function (event) {
    const img = event.target.innerText;
    const found = this.possibleSecondaryColors.filter((el) => el.name === img);
    this.secondaryColors.push(found[0]);
    },

    addAccentImage: function (event) {
    const img = event.target.innerText;
    const found = this.possibleAccentColors.filter((el) => el.name === img);
    this.accentColors.push(found[0]);
    },

    addWheelImage: function (event) {
    const img = event.target.innerText;
    const found = this.possibleWheelTypes.filter((el) => el.name === img);
    this.wheelTypes.push(found[0]);
    },
  },

}; 


  
</script>

<style>

img {
  max-width: 700px;  
  max-height: 700px;
}


</style>