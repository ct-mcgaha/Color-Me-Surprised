<template>
<body v-bind:style="computeRGB">
  <div class="main">
    <h1>Color Me Surprised</h1>
    <button class="button" v-on:click="reloadPage">
        generate <br> random <br> color
        </button>
  <p class="rgbDisplay">{{ computeRGB.backgroundColor }} </p>
  </div>
</body>
</template>

<script>
export default {
    name: "color-me-surprised",
    data() {
        return {
            name: "push the button to generate random color",
            description: "the button will generate a color based on RGB values",
        }
    },
    computed: {
        computeRGB() {
            let rgb = "rgb(" + Math.floor(Math.random() * (256)) + 
            ", " + Math.floor(Math.random() * (256)) + ", " + 
            Math.floor(Math.random() * (256)) + ")";
            return {
            backgroundColor: rgb
            }
        }
    },
    methods: {
        reloadPage() {
            window.location.reload()
        }
        }
    }
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Oswald');
   *{
    padding: 0 !important;
    margin: 0 !important;
    }

body {
    font-family: Oswald;
    color: white;
    text-shadow: 6px 6px 1px black;
    font-weight: bold;
    font-style: italic;
}

p {
    margin: auto;
    padding-top: 15%;
    font-size: 72px;
    height: 10vh;
}

h1 {
    margin-top: auto;
    font-size: 72px;
    padding-bottom: 15%;
    height: 15vh;
}

button {
    padding-top: 5%;
    position: relative;
    height: 360px;
    width: 360px;
    border-radius: 100%;
    font-size: 72px;
    font-family: Oswald;
    font-weight: bold;
    font-style: italic;
    line-height: 93%;
    box-shadow: 6px 6px 1px black;
}

div {
    height: 100vh;
}

.button:hover {background-color: #eeefff}

.button:active {
  transform: translateY(4px);
}
</style>