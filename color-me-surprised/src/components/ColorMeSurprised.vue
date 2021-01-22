<template>
  <div class="main" v-bind:style="computeRGB">Color Me Surprised
    <button class="button">I'm a button!</button>
  <p class="rgbDisplay">test</p>
  </div>
</template>

<script>
export default {
    name: "color-me-surprised",
    data() {
        return {
            name: "push the button to generate random color",
            description: "the button will generate a color based on RGB values"
        }
    },
    computed: {
        computeRGB() {
            return {
             backgroundColor: "rgb(180, 180, 255)"
        }
    }
    }
}
</script>

<style>
p {
    margin: auto;
}
</style>