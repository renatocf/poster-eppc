<template>
  <section class="section">
    <div class="header">
      <h2 class="title">Tech Talks e Code Schools</h2>

      <span class="description">
        Atividade de férias do USPCodeLab, traz palestras sobre ferramentas e
        técnicas a serem utilizadas no desenvolvimento de um projeto com
        múltiplos times durante uma semana de 40h de trabalho
      </span>
    </div>

    <div class="photos">
      <div v-for="index in 9" :key="index" class="photo" :class="`p${index}`"/>
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
  @apply w-full h-72;

  display: grid;

  grid-template-rows: repeat(8, 1fr);
  grid-template-columns: repeat(8, 1fr);
  grid-template-areas:
    "p1 p1 p1 p1 p2 p2 p3 p3"
    "p1 p1 p1 p1 p2 p2 p3 p3"
    "p4 p5 p5 p5 p5 p5 p5 p6"
    "p4 p5 p5 p5 p5 p5 p5 p6"
    "p4 p5 p5 p5 p5 p5 p5 p6"
    "p4 p5 p5 p5 p5 p5 p5 p6"
    "p7 p7 p8 p8 p9 p9 p9 p9"
    "p7 p7 p8 p8 p9 p9 p9 p9";

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
  background-image: url("~@/assets/code-schools/p1.jpg");
}

.p2 {
  grid-area: p2;
  background-image: url("~@/assets/code-schools/p2.jpg");
}

.p3 {
  grid-area: p3;
  background-image: url("~@/assets/code-schools/p3.jpg");
}

.p4 {
  grid-area: p4;
  background-image: url("~@/assets/code-schools/p4.jpg");
}

.p5 {
  grid-area: p5;
  background-image: url("~@/assets/code-schools/p5.jpg");
}

.p6 {
  grid-area: p6;
  background-image: url("~@/assets/code-schools/p6.jpg");
}

.p7 {
  grid-area: p7;
  background-image: url("~@/assets/code-schools/p7.jpg");
}

.p8 {
  grid-area: p8;
  background-image: url("~@/assets/code-schools/p8.jpg");
}

.p9 {
  grid-area: p9;
  background-image: url("~@/assets/code-schools/p9.jpg");
}
</style>
