<template>
  <div class="wrapper">
    <h1>Hi.</h1>
    <h2>My name is Dan Hutchinson.</h2>
    <div class="body-text">
      <p>
        I am a Software Developer in Stafford, UK. Most of my work is created for a company called
        <a
          href="https://codeweavers.net"
          target="_blank"
        >Codeweavers</a>, outside of work I'm usually working on personal projects or messing around with new tech. You
        can find those things on
        <a
          href="https://github.com/danielhutchinson"
          target="_blank"
        >Github</a>
      </p>

      <p>I am also an independent game developer, you can view my work at Pixelbark Games.</p>

      <p>
        You can follow me on
        <a href="https://twitter.com/danwhutchinson" target="_blank">Twitter</a>, if you like.
      </p>

      <p>
        Please send any business enquiries to
        <a
          href="mailto:dan@hutchinson.io"
        >dan@hutchinson.io.</a>
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class App extends Vue {}
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Comfortaa:400,700");

$easing: cubic-bezier(0.445, 0.05, 0.55, 0.95);
$dark-grey: #282C34;
$white: #BBC5CB;
$primary-color: #CD5C63;
$secondary-color: #8EBF67;
$tertiary-color: #C1895A;

body {
  font-family: "Comfortaa";
  line-height: 1.75;
  color: $white;
  background: $dark-grey;
}

h1,
h2,
a {
  color: $primary-color;
}

a {
  text-decoration: none;
  transition: color 350ms $easing;

  &:hover {
    color: lighten($tertiary-color, 10%);
  }
}

h1 {
  opacity: 0;
  font-size: 3em;
  margin-bottom: 0.2em;
  line-height: 1;
  animation: fade-in 350ms $easing forwards;
}

h2 {
  opacity: 0;
  font-size: 2em;
  animation: fade-in 350ms $easing forwards;
  animation-delay: 150ms;
}

.body-text {
  opacity: 0;
  margin-top: 10px;
  animation: fade-in 350ms $easing forwards;
  animation-delay: 350ms;
}

.wrapper {
  padding: 10em 10em 3em 10em;
  width: 740px;
}

@keyframes fade-in {
  0% {
    margin-top: 10px;
    opacity: 0;
  }

  100% {
    margin-top: 0;
    opacity: 1;
  }
}
</style>
