<template>
  <section class="section">
    <div class="header">
      <h2 class="title">HackathonUSP</h2>

      <span class="description">
        Maior evento do USPCodeLab, voltado para USPianos de diversos cursos,
        patrocinado pela reitoria da USP e empresas parceiras, focado em quem
        vai participar de um hackathon pela primeira vez
      </span>
    </div>

    <div class="photos">
      <div v-for="index in 5" :key="index" class="photo" :class="`p${index}`"/>
    </div>
  </section>
</template>

<style scoped>
.section {
  @apply p-6 border-2 rounded;
  @apply flex flex-col justify-between items-center;
}

.header {
  @apply flex flex-col justify-center items-center;
}

.title {
  @apply mb-3;
  @apply font-title;
  @apply text-center;
}

.description {
  @apply mb-3;
  @apply text-center leading-normal;
}

.photos {
  @apply flex-grow;
  @apply w-full h-64;

  display: grid;

  grid-template-rows: repeat(5, 1fr);
  grid-template-columns: repeat(6, 1fr);
  grid-template-areas:
    "p1 p1 p1 p3 p4 p4"
    "p1 p1 p1 p3 p4 p4"
    "p1 p1 p1 p5 p5 p5"
    "p2 p2 p2 p5 p5 p5"
    "p2 p2 p2 p5 p5 p5";

  grid-row-gap: 0.25rem;
  grid-column-gap: 0.25rem;
}

.photo {
  @apply h-full w-full;
  background-size: cover;
  background-position: center;
}

.p1 {
  grid-area: p1;
  background-image: url("~@/assets/hackathonusp/p1.jpg");
}

.p2 {
  grid-area: p2;
  background-image: url("~@/assets/hackathonusp/p2.jpg");
}

.p3 {
  grid-area: p3;
  background-image: url("~@/assets/hackathonusp/p3.jpg");
}

.p4 {
  grid-area: p4;
  background-image: url("~@/assets/hackathonusp/p4.jpg");
}

.p5 {
  grid-area: p5;
  background-image: url("~@/assets/hackathonusp/p5.jpg");
}
</style>
