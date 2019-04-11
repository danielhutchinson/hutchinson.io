<template>
  <div class="wrapper">
    <div class="bubble"></div>
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
        >Github.</a>
      </p>

      <p>
        I am also an independent game developer, you can see my games over at
        <a
          href="https://pixelbark.games"
          target="_blank"
        >Pixelbark Games</a>.
      </p>

      <p>
        You can follow me on
        <a href="https://twitter.com/danwhutchinson" target="_blank">Twitter</a>, if you like.
      </p>

      <p>
        Please send any business enquiries to
        <a href="mailto:dan@hutchinson.io">dan@hutchinson.io.</a>
      </p>

      <p>
        If you're a recruiter you can attempt to contact me on
        <a href="https://www.linkedin.com/in/danhutch/" target="_blank">LinkedIn</a>
      </p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class App extends Vue {}
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Comfortaa:400,700");

$easing: cubic-bezier(0.445, 0.05, 0.55, 0.95);
$dark-grey: #282c34;
$white: #bbc5cb;
$primary-color: #cd5c63;
$secondary-color: #8ebf67;
$tertiary-color: #c1895a;

body,
html {
  font-family: "Comfortaa";
  line-height: 1.75;
  color: $white;
  background: $dark-grey;
  overflow-x: hidden;
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
  padding-top: 3em;
  width: 90%;
  margin: 0 auto;

  @media screen and (min-width: 768px) {
    padding: 10em 10em 3em 10em;
    width: 60%;
    margin: 0;
  }
}

.bubble {
  position: fixed;
  top: -350px;
  left: -250px;
  border-radius: 100%;
  background: lighten($dark-grey, 10%);
  opacity: 0.1;
  height: 1000px;
  width: 1000px;
  animation: pulse 7s $easing infinite;
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

@keyframes pulse {
  0% {
    transform: scale(1);
  }

  50% {
    transform: scale(1.1);
  }

  100% {
    transform: scale(1);
  }
}
</style>
