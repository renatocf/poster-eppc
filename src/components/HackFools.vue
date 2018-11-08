<template>
  <section class="section">
    <div class="header">
      <h2 class="title">HackFools</h2>

      <span class="description">
        Hackday com 10h de duração, voltado para ingressantes, realizado numa
        empresa parceira, busca incentivar os alunos a aplicarem seus
        conhecimentos para a resolução de problemas
      </span>
    </div>

    <div class="photos">
      <div v-for="index in 4" :key="index" class="photo" :class="`p${index}`"/>
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

  grid-template-rows: repeat(4, 1fr);
  grid-template-columns: repeat(8, 1fr);
  grid-template-areas:
    "p1 p1 p1 p1 p2 p2 p3 p3"
    "p1 p1 p1 p1 p2 p2 p3 p3"
    "p1 p1 p1 p1 p4 p4 p4 p4"
    "p1 p1 p1 p1 p4 p4 p4 p4";

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
  background-image: url("~@/assets/hackfools/p1.jpg");
}

.p2 {
  grid-area: p2;
  background-image: url("~@/assets/hackfools/p2.jpg");
}

.p3 {
  grid-area: p3;
  background-image: url("~@/assets/hackfools/p3.jpg");
}

.p4 {
  grid-area: p4;
  background-image: url("~@/assets/hackfools/p4.jpg");
}
</style>
