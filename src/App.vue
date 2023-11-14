<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import ParaIntro from "@/components/ParaIntro.vue";

import {reactive} from "vue";
import Destination from "@/components/Destination.vue";

// Datas
const destinations = reactive([
  {
    id: 1,
    nom: 'Malaga',
    prix: 890,
    description: 'Malaga est une ville du sud de l\'Espagne, sur la Costa del Sol, connue pour ses plages et ses stations balnéaires.'
  },
  {
    id: 2,
    nom: 'Honolulu',
    prix: 3890,
    description: 'Honolulu est la capitale et la plus grande ville de l\'État d\'Hawaï, aux États-Unis. Située sur la côte sud de l\'île d\'Oahu, elle est le centre des affaires, du commerce et du divertissement d\'Hawaï.'
  },
  {
    id: 3,
    nom: 'Oslo',
    prix: 1290,
    description: 'Oslo, la capitale et la plus grande ville de Norvège, est située à la pointe sud du fjord d\'Oslo. Entourée de collines verdoyantes et de forêts, elle possède de nombreux parcs et espaces verts.'
  },
  {
    id: 4,
    nom: 'Bora-Bora',
    prix: 5490,
    description: 'Bora-Bora est une petite île volcanique de l\'archipel de la Société en Polynésie française. Entourée d\'un lagon et d\'une barrière de corail, elle est célèbre pour ses plages de sable blanc bordées de cocotiers et ses bungalows sur pilotis.'
  },
  {
    id: 5,
    nom: 'Paris',
    prix: 590,
    description: 'Paris, capitale de la France, est une grande ville européenne et un centre mondial de l\'art, de la mode, de la gastronomie et de la culture. Son paysage urbain du XIXe siècle est traversé par de larges boulevards et la Seine.'
  },
  {
    id: 6,
    nom: 'Londres',
    prix: 490,
    description: 'Londres, la capitale de l\'Angleterre et du Royaume-Uni, est une ville moderne dont l\'histoire remonte à l\'époque romaine. En son centre se dressent l\'imposant Parlement, l\'emblématique Big Ben et l\'abbaye de Westminster, lieu de couronnement des monarques britanniques.'
  }
]);
</script>

<template>
  <h1>Destinations de vacances</h1>

  <destination
      v-for="destPar in destinations"
      :key="destPar.id"
      :p-dest="destPar"
  />

  <!--
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
    <h1>Toto</h1>
    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
  -->
</template>

<style scoped>
h1 {
  color: darkcyan;
}
/*
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
 */
</style>
