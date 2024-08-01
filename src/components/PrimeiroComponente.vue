<template>
  <h1>{{ title }}</h1>
  <h2>{{ subtitle }}</h2>
  <p>{{ description }}</p>
  <MultiplosEventos />
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue';
export default {
  name: 'PrimeiroComponente',
  components: {
    MultiplosEventos,
  },
  data() {
    return {
      title: 'Fabio Vige',
      subtitle: 'Desenvolvedor Web',
      description: 'Simplicidade e funcionalidades caminham juntos',
    };
  },
};
</script>
