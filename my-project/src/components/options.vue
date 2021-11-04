<template>
  <div class="color">
  <div class="color-options">
  <h2>Main Colors:</h2>
  <ul>
    <li 
    class="main-color" 
    v-for="mainColor in mainColorsChoices" 
    :key="mainColor.name" v-on:click="addMainImage"> {{mainColor.name}} 
    </li>
   </ul>

   <h2>Secondary Colors:</h2>
  <ul>
    <li 
    class="secondary-color" 
    v-for="secondaryColor in secondaryColorsChoices" 
    :key="secondaryColor.name" v-on:click="addSecondaryImage"> {{secondaryColor.name}} 
    </li>
  </ul>

  <h2>Accent Colors:</h2>
  <ul>
    <li 
    class="accent-color" 
    v-for="accentColor in accentColorsChoices" 
    :key="accentColor.name" v-on:click="addAccentImage"> {{accentColor.name}} 
    </li>
   </ul>

  <h2>Chose A Wheel Type:</h2>
  <ul>
    <li 
    class="wheel-type" 
    v-for="wheelType in wheelTypesChoices" 
    :key="wheelType.name" v-on:click="addWheelImage"> {{wheelType.name}} 
    </li>
   </ul>
  </div>

  <div class="color-image">
  <ul>
    <div class="main-image" v-for="mainColor in mainColorsSelected" :key="mainColor.image">
    <img :src="mainColor.image" alt="" />
    </div>
  </ul>
  <ul>
    <div class="secondary-image" v-for="secondaryColor in secondaryColorsSelected" :key="secondaryColor.image">
    <img :src="secondaryColor.image" alt="" />
    </div>
  </ul>
  <ul>
    <div class="accent-image" v-for="accentColor in accentColorsSelected" :key="accentColor.image">
    <img :src="accentColor.image" alt="" />
    </div>
  </ul>
  <ul>
    <div class="wheel-image" v-for="wheelType in wheelTypesSelected" :key="wheelType.image">
    <img :src="wheelType.image" alt="" />
    </div>
  </ul>
  </div>
   
  </div>
  </template>
  


<script>
export default {
  name: "options",

  data() {
    return {
      mainColorsSelected: [],
      mainColorsChoices: [
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
          name: "Greeen",
          image: require("../assets/main/mainGreen.png"),
        },
        {
          name: "Purple",
          image: require("../assets/main/mainPurple.png"),
        },
      ],

      secondaryColorsSelected: [], 
      secondaryColorsChoices: [
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
      

      accentColorsSelected: [], 
      accentColorsChoices: [
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

      wheelTypesSelected: [],
      wheelTypesChoices: [
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
    let img = event.target.innerText;
    let added = this.mainColorsChoices.filter(element => element.name === img);
    this.mainColorsSelected.push(added[0]);
    },

    addSecondaryImage: function (event) {
    let img = event.target.innerText;
    let added = this.secondaryColorsChoices.filter(element => element.name === img);
    this.secondaryColorsSelected.push(added[0]);
    },

    addAccentImage: function (event) {
    let img = event.target.innerText;
    let added = this.accentColorsChoices.filter(element => element.name === img);
    this.accentColorsSelected.push(added[0]);
    },

    addWheelImage: function (event) {
    let img = event.target.innerText;
    let added = this.wheelTypesChoices.filter(element => element.name === img);
    this.wheelTypesSelected.push(added[0]);
    },
  },

}; 


  
</script>

<style>

img {
  max-width: 700px;  
  max-height: 700px;
  position: absolute;
  top: 100px;
  left: 230px;
}

.color-options {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

.color {
  padding-left: 60px; 
  margin-top: 80px;
}

.main-color, .secondary-color, .accent-color, .wheel-type {
  list-style: none;
}

</style>