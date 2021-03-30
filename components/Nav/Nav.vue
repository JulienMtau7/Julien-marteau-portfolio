<template>
  <div class="header">
    <div class="header__header">
      <img src="@/assets/img/mj-logo.png" alt="logo_Marteau-Julien">
      <div
        id="menu-btn"
        class="menu-btn disable"
        @click="addClassNav"
      >
        <div class="menu-btn__burger"></div>
      </div>
    </div>

    <img  class="logo-desktop" src="@/assets/img/mj-logo.png" alt="logo_Marteau-Julien">

    <nav id="nav" class="nav disable">
      <ul>
        <li @click="addClassNav"><NuxtLink to="/" exact>Home</NuxtLink></li>
        <li @click="addClassNav"><NuxtLink to="/about" exact>About</NuxtLink></li>
        <li @click="addClassNav"><NuxtLink to="/contact" exact>Contact</NuxtLink></li>
      </ul>

      <!-- <label class="power">
        <input type="checkbox">
        <div>
            <svg viewBox="0 0 44 44">
                <path d="M22,6 C31,6 38,13 38,22 C38,31 31,38 22,38 C13,38 6,31 6,22 C6,13 13,6 22,6 L22,28" id="path"></path>
            </svg>
        </div>
      </label> -->
    </nav>
  </div>
</template>

<script>
  export default {
    name: "Nav",

    methods: {
      addClassNav(){
        let navSelected = document.querySelector('#nav')
        let buttonSelected = document.querySelector('#menu-btn')
        let larg = (document.body.clientWidth)

        if(larg < 700) {

          if (navSelected.classList.contains('disable') && buttonSelected.classList.contains('disable')) {

            navSelected.classList.add('active')
            navSelected.classList.remove('disable')

            buttonSelected.classList.add('active')
            buttonSelected.classList.remove('disable')



          } else if (navSelected.classList.contains('active') && buttonSelected.classList.contains('active')) {

            navSelected.classList.add('disable')
            navSelected.classList.remove('active')

            buttonSelected.classList.add('disable')
            buttonSelected.classList.remove('active')

          }
        }

      }
    }
  }

</script>

<style src="./nav.scss" lang="scss">
</style>
