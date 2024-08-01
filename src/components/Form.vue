<template>
  <div>
    <h1>Componente Form</h1>
    <h2>Cadastro de pessoa</h2>
    <form>
      <div><InputText /></div>
      <div><InputText /></div>
      <ButtonSubmit />
    </form>
  </div>
</template>

<script>
import InputText from './form/InputText.vue';
import ButtonSubmit from './form/ButtonSubmit.vue';
export default {
  name: 'FormPessoa',
  components: {
    InputText,
    ButtonSubmit,
  },
};
</script>
