<script lang="ts" setup>
import GlitchedWriter from "vue-glitched-writer";
import Person from "./components/Person.vue";
import {onMounted} from "vue";

const glitchedWriterOptions = {
  letterize: true,
  delay: 1500,
};

const people = [
  {
    name: "La Badessa Alessandro",
    description: "Professore di Meccanica"
  }, {
    name: "Salvetti Lapo",
    description: "Professore di Telecomunicazioni"
  }, {
    name: "Ciaramella Simona",
    description: "Professoressa di Italiano"
  }, {
    name: "Baldi Maria Cristina",
    description: "Professoressa di Italiano"
  }, {
    name: "Mascioni Fosco",
    description: "Vicepreside e Professore di Logistica"
  }, {
    name: "Nocentini Matassini Daniele",
    description: "Professore di Meccanica"
  }, {
    name: "Lerario Francesca",
    description: "Professoressa di Elettrotecnica"
  }, {
    name: "Dallai Nada",
    description: "Professoressa di Matematica"
  },
]

//Fix for scroll animation
onMounted(() => {
  window.scroll(0, 0);
});
</script>

<template>
  <div id="first" class="fullPageSection">
    <img v-motion-pop :delay="800" alt="Immagine di un cuore" class="centered" src="./assets/heart.svg">
    <GlitchedWriter :options="glitchedWriterOptions" appear class="text" preset="neo" text="Meucci Nel Cuore"/>
  </div>
  <Person v-for="(person) in people" :description="person.description" :name="person.name"/>
</template>

<style lang="scss" scoped>
.fullPageSection {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100%;
  top: 0;
  left: 0;
}

#first {
  .text {
    font-size: 7.5vmin;
    font-weight: 100;
    margin-top: -5vh;
    color: #FAFAFA;
    position: absolute;
  }

}

.centered {
  display: block;
  margin: auto;
  width: 80vmin;
}
</style>
<style lang="scss">
//Glitched writer
.gw-glitched {
  color: #757575;
}
</style>
