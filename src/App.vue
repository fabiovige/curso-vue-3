<template>
  <PrimeiroComponente />
  <LifeCycle />
  <PessoaComponente />
  <FormPessoa />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import LifeCycle from './components/LifeCycle.vue';
import PessoaComponente from './components/Pessoa.vue';
import FormPessoa from './components/Form.vue';

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LifeCycle,
    PessoaComponente,
    FormPessoa,
  },
  data() {
    return {
      name: 'Olá Mundo',
    };
  },
};
</script>
