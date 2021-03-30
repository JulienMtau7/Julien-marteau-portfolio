<template>
    <div class="about__content">
      <section class="section-text">

        <div class="section-text__content">
          <h2>About me</h2>

            <div class="resume">
              <p>Fin 2019, je commence à m'intéresser au développement web à travers les formations d'Openclassrooms sur le Html et le Css. Je me découvre une réelle passion pour ce domaine et je m'engage donc dans une formation intensive qui m'a permis  de renforcer mes bases en Html, Css et Javascript, et d'apprendre de nouvelles technologies. J'ai aussi vu la méthode de travail Agile et l'utilisation de Github. Pendant cette formation je me suis spécialisé sur du React et vu redux, les Hooks, le Scss, etc.</p>
              <p>Je me suis ensuite intéressé au framework Vue.js et Nuxt.js que j'ai tout de suite adoré.</p>
              <p>Aujourdhui, mon objectif est d'acquérir de nouvelles compétences sur les technologies que je connais déjà ou sur d'autres stack. Je suis donc à la recherche d'une première expérience en tant que développeur web front end, stagiaire ou salarié.</p>
            </div>

          <span class="buttonCV">
            <a class="buttonCV__link" target="_blank" href="https://www.fichier-pdf.fr/2021/03/24/cv-marteau/cv-marteau.pdf">Mon Cv</a>
          </span>
        </div>
      </section>
      <section class="section-work">
        <h2>My Work</h2>
        <Carousel />
      </section>
      <section class="section-skills">
        <h2>Skills</h2>

        <div class="wrapperSkills">
          <div><img src="@/assets/img/html-svg.svg" alt="html-svg"><p>Html</p></div>
          <div><img src="@/assets/img/css-svg.svg" alt="css-svg"><p>Css</p></div>
          <div><img src="@/assets/img/js-svg.svg" alt="js-svg"><p>Javascript</p></div>
          <div><img src="@/assets/img/vue-svg.svg" alt="vue-svg"><p>Vue.js</p></div>
          <div><img src="@/assets/img/nuxt-svg.svg" alt="nuxt-svg"><p>Nuxt.js</p></div>
          <div><img src="@/assets/img/react-svg.svg" alt="react-svg"><p>React</p></div>
          <div><img src="@/assets/img/redux-svg.svg" alt="redux-svg"><p>Redux</p></div>
          <div><img src="@/assets/img/sass-svg.svg" alt="sass-svg"><p>Sass</p></div>
          <div><img src="@/assets/img/node-svg.svg" alt="node-svg"><p>Node.js</p></div>
          <div><img src="@/assets/img/responsive-svg.svg" alt="responsive-svg"><p>Responsive Design</p></div>
          <div><img src="@/assets/img/github-svg.svg" alt="github-svg"><p>Github</p></div>
          <div><img src="@/assets/img/agile-svg.svg" alt="agile-svg"><p>Agile</p></div>
        </div>
      </section>
    </div>
</template>

<script>
  import Carousel from '@/components/Carousel/Carousel'

  export default {
    name: "About",

    components: {
      Carousel,
    }
  }
</script>

<style src="./about.scss" lang="scss">

</style>
