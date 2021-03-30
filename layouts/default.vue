<template>
  <div class="defaultVue">
    <Nav />
    <vue-particles
      color="#4e9aff"
      :particleOpacity="1"
      linesColor="#4e9aff"
      :particlesNumber="20"
      shapeType="circle"
      :particleSize="1.5"
      :linesWidth="1"
      :lineLinked="true"
      :lineOpacity=".5"
      :linesDistance="200"
      :moveSpeed="1"
    ></vue-particles>
    <Nuxt />
  </div>
</template>

<script>
  import VueParticles from '../vue-particles/vue-particles'

  export default {
    name: "default",

    components: {
      VueParticles,
    }
  }
</script>

<style lang="scss">
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;

    body {
      color: white;
      font-family: 'Catamaran', sans-serif;
      position: relative;
      overflow: hidden;
      overflow-y: scroll;
      background: linear-gradient(to right, #252d3a, #0a0c0e);
      height: 100vh;

      & .particles-js{
        position: absolute;
        top: 0;
        height: 100vh; width: 100vw;
        z-index: -1;
      }
    }
  }


</style>
