<template>
  <PrimeiroComponente />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue';

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
  },
  data() {
    return {
      name: 'Olá Mundo',
    };
  },
};
</script>
