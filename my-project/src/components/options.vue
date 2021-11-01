<template>
  <div id="option">
    <h2>
      {{ mainColors }}
    </h2>
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
          image: require("../assets/main/mainred.png"),
        },
        {
          name: "Blue",
          image: require("../assets/main/mainblue.png"),
        },
        {
          name: "Pink",
          image: require("../assets/main/mainpink.png"),
        },
        {
          name: "Orange",
          image: require("../assets/main/mainorange.png"),
        },
        {
          name: "Green",
          image: require("../assets/main/maingreen.png"),
        },
        {
          name: "Purple",
          image: require("../assets/main/mainpurple.png"),
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
          image: require("../assets/accent/whiteAccent.png"),
        },
        {
          name: "Black",
          image: require("../assets/accent/blackA.png"),
        },
        {
          name: "Grey",
          image: require("../assets/accent/accentGrey.png"),
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
};
</script>