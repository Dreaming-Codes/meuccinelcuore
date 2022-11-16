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
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam sit amet dapibus eros. Vestibulum vitae cursus lorem, vitae ornare enim. Integer gravida quam sem, quis tristique nisi volutpat vitae. Nam pharetra id eros ac blandit. Donec id tellus ipsum. Cras."
  }, {
    name: "Salvetti Lapo",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam sit amet dapibus eros. Vestibulum vitae cursus lorem, vitae ornare enim. Integer gravida quam sem, quis tristique nisi volutpat vitae. Nam pharetra id eros ac blandit. Donec id tellus ipsum. Cras."
  }, {
    name: "Ciaramella Simona",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam sit amet dapibus eros. Vestibulum vitae cursus lorem, vitae ornare enim. Integer gravida quam sem, quis tristique nisi volutpat vitae. Nam pharetra id eros ac blandit. Donec id tellus ipsum. Cras."
  }, {
    name: "Baldi Maria Cristina",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam sit amet dapibus eros. Vestibulum vitae cursus lorem, vitae ornare enim. Integer gravida quam sem, quis tristique nisi volutpat vitae. Nam pharetra id eros ac blandit. Donec id tellus ipsum. Cras."
  }, {
    name: "Mascioni Fosco",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam sit amet dapibus eros. Vestibulum vitae cursus lorem, vitae ornare enim. Integer gravida quam sem, quis tristique nisi volutpat vitae. Nam pharetra id eros ac blandit. Donec id tellus ipsum. Cras."
  }, {
    name: "Nocentini Matassini Daniele",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam sit amet dapibus eros. Vestibulum vitae cursus lorem, vitae ornare enim. Integer gravida quam sem, quis tristique nisi volutpat vitae. Nam pharetra id eros ac blandit. Donec id tellus ipsum. Cras."
  }, {
    name: "Lerario Francesca",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam sit amet dapibus eros. Vestibulum vitae cursus lorem, vitae ornare enim. Integer gravida quam sem, quis tristique nisi volutpat vitae. Nam pharetra id eros ac blandit. Donec id tellus ipsum. Cras."
  }, {
    name: "Dallai Nada",
    description: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam sit amet dapibus eros. Vestibulum vitae cursus lorem, vitae ornare enim. Integer gravida quam sem, quis tristique nisi volutpat vitae. Nam pharetra id eros ac blandit. Donec id tellus ipsum. Cras."
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
