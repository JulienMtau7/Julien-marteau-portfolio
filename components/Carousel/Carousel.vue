<template>
  <div class="carousel">

    <img @click="displayMask" src="@/assets/img/social-media.png" alt="screen_socialmedia" class="active">
    <div @click="removeClikedMask" class="mask active">
      <h2>Social Media Dashboard</h2>
      <p>Challenge d'un dashboard avec un theme switcher, proposé par le site <a href="https://www.frontendmentor.io/" target="_blank">frontendmentor.io</a></p>

      <span class="buttonProject">
        <a class="linkProject" href="https://frontend-mentor-social-media-dashboard-with-theme-switcher.vercel.app/" target="_blank">Lien du projet</a>
      </span>
    </div>

    <img @click="displayMask" src="@/assets/img/CryptoMatch.png" alt="screen_cryptomatch">
    <div @click="removeClikedMask" class="mask">
      <h2>Crypto Match</h2>
      <p>Site de trading de cryptomonnaie réalisé dans le cadre du projet de fin de formation de mon école</p>

      <span class="buttonProject">
        <a class="linkProject" href="http://cryptomatch.surge.sh/" target="_blank">Lien du projet</a>
      </span>
    </div>

    <img @click="displayMask" src="@/assets/img/github-api.png" alt="screen_githubApi">
    <div @click="removeClikedMask" class="mask">
      <h2>Github api search</h2>
      <p>Page permettant de rechercher un repo sur github</p>

      <span class="buttonProject">
        <a class="linkProject" href="http://api-github-oclock.surge.sh/" target="_blank">Lien du projet</a>
      </span>
    </div>

    <img @click="displayMask" src="@/assets/img/Loopstudio.png" alt="screen_loppstudio">
    <div @click="removeClikedMask" class="mask">
      <h2>Loopstudios</h2>
      <p>Challenge d'une page d'accueil, proposé par le site <a href="https://www.frontendmentor.io/" target="_blank">frontendmentor.io</a></p>

      <span class="buttonProject">
        <a class="linkProject" href="https://loopstudios-landing-page-main-frontend-mentor.vercel.app/" target="_blank">Lien du projet</a>
      </span>
    </div>

    <div class="btn-nav left" @click="prev">←</div>
    <div class="btn-nav right" @click="next">→</div>
  </div>
</template>

<script>
  export default {
    name: "Carousel",

    data(){
      return {
        items: "",
        nbSlide: 0,
        count: 0,

        itemsDiv: "",
        nbSlideDiv: 0,
        countDiv: 0,

      }
    },

    mounted(){
      this.items = document.querySelector('.carousel').querySelectorAll('img')
      this.nbSlide = this.items.length

      this.itemsDiv = document.querySelector('.carousel').querySelectorAll('.mask')
      this.nbSlideDiv = this.itemsDiv.length
    },

    methods: {
      next(){
        this.items[this.count].classList.remove('active')
        this.itemsDiv[this.countDiv].classList.remove('active')


        if(this.count < this.nbSlide - 1 && this.countDiv < this.nbSlideDiv - 1){
          this.count++
          this.countDiv++

        } else {
          this.count = 0
          this.countDiv = 0
        }

        this.items[this.count].classList.add('active')
        this.itemsDiv[this.countDiv].classList.add('active')

      },

      prev(){
        this.items[this.count].classList.remove('active')
        this.itemsDiv[this.countDiv].classList.remove('active')

        if(this.count > 0 && this.countDiv > 0){
          this.count--
          this.countDiv--

        } else {
          this.count = this.nbSlide -1
          this.countDiv = this.nbSlideDiv -1
        }

        this.items[this.count].classList.add('active')
        this.itemsDiv[this.countDiv].classList.add('active')
      },

      displayMask(){
        this.itemsDiv[this.countDiv].classList.add('clicked')
      },

      removeClikedMask(){
        this.itemsDiv[this.countDiv].classList.remove('clicked')
      }
    }

  }
</script>

<style src="./carousel.scss" lang="scss">

</style>
