<template>
  <section class="section">
    <div class="header">
      <h2 class="title">dev.journey()</h2>

      <span class="description">
        Programa de 6 fases que visa introduzir e amadurecer os conhecimentos
        dos alunos da USP sobre desenvolvimento de software
      </span>
    </div>

    <div v-for="phase of phases" :key="phase.name" class="phase">
      <img :src="require(`@/assets/dev-journey/${phase.name}.svg`)"
           :alt="phase.name" class="phase_logo"
      >
      <div v-html="phase.description" class="phase_description" /> <!-- eslint-disable-line -->
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

.phases {
  @apply flex-grow;
  @apply flex flex-col justify-between items-center;
}

.phase {
  @apply p-3 border rounded;
  @apply flex flex-row items-center;
}

.phase_logo {
  @apply h-24 mr-4;
}

.phase_description {
  @apply leading-normal;
}
</style>

<script>
export default {
  data() {
    return {
      phases: {
        start: {
          name: "dev-start",
          description:
            "<strong>Ciclo de oficinas de introdução à programação web</strong> para o público geral da universidade, com tópicos como HTML, CSS e JavaScript"
        },
        learn: {
          name: "dev-learn",
          description:
            "<strong>Grupos de estudo com reuniões semanais</strong> para desenvolvimento de projetos supervisionados pela organização do grupo"
        },
        boost: {
          name: "dev-boost",
          description:
            "<strong>Grupo de estudos avançado com projetos em times</strong> para aprendizado de técnicas de modelagem e implementação de sistemas"
        },
        camp: {
          name: "dev-camp",
          description:
            "<strong>Escola de férias</strong> que serve de formatura para os alunos do dev.learn() e dev.boost(), que trabalham num projeto multi-time de grande porte"
        },
        hire: {
          name: "dev-hire",
          description:
            "<strong>Iniciativa de aproximação empresa-universidade</strong> para ajudar os alunos a se prepararem para o mercado (estágios e empregos)"
        },
        research: {
          name: "dev-research",
          description:
            "<strong>Iniciativa de pesquisa</strong> para ajudar os graduandos a conhecerem e se engajarem com a produção acadêmica (iniciações científicas e TCCs)"
        }
      }
    };
  }
};
</script>
