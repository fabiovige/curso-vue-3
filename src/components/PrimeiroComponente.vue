<template>
  <h1>{{ title }}</h1>
  <h2>{{ subtitle }}</h2>
  <p>{{ description }}</p>
</template>

<script>
export default {
  name: 'PrimeiroComponente',
  data() {
    return {
      title: 'Fabio Vige',
      subtitle: 'Desenvolvedor Web',
      description: 'Simplicidade e funcionalidades caminham juntos',
    };
  },
};
</script>
