<template>
  <div>
    <h2>Componente Pessoa</h2>
    <InfoPessoa />
  </div>
</template>

<script>
import InfoPessoa from './Info.vue';

export default {
  name: 'PessoaComponente',
  components: {
    InfoPessoa,
  },
  data() {
    return {
      name: 'Nega',
    };
  },
};
</script>
