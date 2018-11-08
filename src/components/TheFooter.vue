<template>
  <footer class="footer">
    <div class="mark">
      <img src="@/assets/logos/ucl-logo-wb-alpha.svg" alt="Logo UCL"
           class="mark_logo">
      <div class="mark_mission">
        Estimulando a inovação tecnológica na USP
      </div>
      <div class="mark_email">
        https://codelab.ime.usp.br
      </div>
    </div>

    <div class="supporters">
      <div class="supporters_title">Apoio:</div>
      <div class="supporters_logos">
        <img class="supporter" src="@/assets/supporters/prp.png">
        <img class="supporter" src="@/assets/supporters/prg.png">
        <img class="supporter" src="@/assets/supporters/capes.jpg">
      </div>
    </div>

    <div class="cards"/>
  </footer>
</template>

<style scoped>
.footer {
  @apply bg-dark text-light;
  @apply flex flex-row justify-between items-center;
}

.mark {
  @apply flex flex-col justify-center items-center;
}

.mark_logo {
  @apply h-16;
}

.mark_mission {
  @apply text-center;
  @apply mb-2;
}

.mark_email {
  @apply text-sm;
}

.supporters {
  @apply h-full;
  @apply flex flex-col justify-between items-start;
}

.supporters_logos {
  @apply p-1;
  @apply bg-light rounded-lg;
  @apply flex flex-row justify-around items-center;
}

.supporter {
  @apply h-24;
  @apply mx-2;
}

.cards {
  @apply h-full;
  @apply border border-dashed;
  width: 8cm;
}
</style>
