<template>
  <div id="app">
    <TheNavbar id="navbar"/>
    <main id="main">
      <About id="about"/>
      <DevJourney id="dev-journey"/>
      <HackFools id="hackfools"/>
      <WinterSchool id="winter-school"/>
      <HackathonUSP id="hackathon-usp"/>
    </main>
    <TheFooter id="footer"/>
  </div>
</template>

<script>
import TheNavbar from "@/components/TheNavbar.vue";
import About from "@/components/About.vue";
import DevJourney from "@/components/DevJourney.vue";
import HackFools from "@/components/HackFools.vue";
import WinterSchool from "@/components/WinterSchool.vue";
import HackathonUSP from "@/components/HackathonUSP.vue";
import TheFooter from "@/components/TheFooter.vue";

export default {
  name: "App",
  components: {
    TheNavbar,
    About,
    DevJourney,
    HackFools,
    WinterSchool,
    HackathonUSP,
    TheFooter
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Montserrat");

html {
  font-size: 18pt;
}

body {
  width: 594mm;
  height: 841mm;
}

#app {
  @apply w-full h-full;
}

#navbar {
  @apply w-full h-1/10;
  @apply py-10 px-16;
}

#footer {
  @apply w-full h-1/10;
  @apply py-10 px-16;
}

#main {
  @apply w-full h-4/5;
  @apply p-16;

  display: grid;
  grid-template-rows: repeat(7, 1fr);
  grid-template-columns: repeat(3, 1fr);
  grid-template-areas:
    "about       hackfools hackfools"
    "about       hackfools hackfools"
    "dev-journey winter-school winter-school"
    "dev-journey winter-school winter-school"
    "dev-journey winter-school winter-school"
    "dev-journey hackathon-usp hackathon-usp"
    "dev-journey hackathon-usp hackathon-usp";

  grid-row-gap: 2rem;
  grid-column-gap: 2rem;
}

#about {
  grid-area: about;
}

#dev-journey {
  grid-area: dev-journey;
}

#hackfools {
  grid-area: hackfools;
}

#winter-school {
  grid-area: winter-school;
}

#hackathon-usp {
  grid-area: hackathon-usp;
}
</style>
