<template>
  <div>
    <h1>Componente Form</h1>
    <h2>Cadastro de pessoa</h2>
    <form @submit="enviarFormulario($event)">
      <div><input type="text" v-model="name"></div>
      <div><input type="text" v-model="email"></div>
      <ButtonSubmit />
    </form>
  </div>
</template>

<script>
import ButtonSubmit from './form/ButtonSubmit.vue';
export default {
  name: 'FormPessoa',
  components: {
    ButtonSubmit,
  },
  data() {
    return {
      name: '',
      email: '',
    };
  },
  methods: {
    enviarFormulario(e) {
      e.preventDefault();

      console.log('Formulário enviado');
      console.log('Nome:', this.name);
      console.log('Email:', this.email);
    },
  },
};
</script>
