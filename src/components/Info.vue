<template>
  <div>
    <h3>Componente Info</h3>
    <p v-if="esta_trabalhando"><strong>Status:</strong> Estou trabalhando nesse momento</p>
    <p v-else>Buscando oportunidades</p>

    <div v-show="mostrar_tecnologias">
      <h3>Tecnologias</h3>
      <p>Utilizo as seguintes tecnologias:</p>
      <ul>
        <li>JavaScript</li>
        <li>PHP</li>
        <li>HTML</li>
      </ul>
    </div>
    <p>Acesse meu portifólio: <a v-bind:href="meu_link" target="_blank">Meu Pertifólio</a></p>
    <Picture />
  </div>
</template>

<script>
import Picture from './Picture.vue';
export default {
  name: 'InfoPessoa',
  components: {
    Picture,
  },
  data() {
    return {
      esta_trabalhando: true,
      mostrar_tecnologias: true,
      meu_link: 'https://www.linkedin.com/',
    };
  },
};
</script>
