<template>
  <nav class="navbar">
    <img src="@/assets/logos/ucl-mark-alpha.svg" alt="UCL Logo" class="logo">
    <div class="header">
      <h1 class="title">USPCodeLab</h1>
      <h2 class="subtitle">Ensino, Pesquisa e Extensão pela Inovação Tecnológica na USP</h2>
    </div>

    <div class="authors">
      <div class="student">
        <strong>Renato Cordeiro Ferreira</strong>
        <br><span class="email">renatocf@ime.usp.br</span>
        <br><span class="institute">IME-USP</span>
      </div>
      <div class="advisor">
        <strong>Alfredo Goldman</strong>
        <br><span class="email">gold@ime.usp.br</span>
        <br><span class="institute">IME-USP</span>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  @apply bg-primary;
  @apply text-light;
  @apply flex flex-row justify-around items-center;
}

.logo {
  @apply h-full;
  @apply rounded-full;
}

.title {
  @apply font-bold font-title text-5xl;
  @apply mb-2;
}

.subtitle {
  @apply font-title;
}

.authors {
  @apply h-full;
  @apply flex flex-col justify-around items-start;
}

.email {
}

.institute {
  @apply text-xs;
}
</style>
