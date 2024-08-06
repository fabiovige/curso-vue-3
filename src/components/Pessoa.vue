<template>
  <div>
    <h2>Componente Pessoa</h2>
    <InfoPessoa :email="email" />
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
      email: 'fabiovigedev@gmail.com'
    };
  },
};
</script>
