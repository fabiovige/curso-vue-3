<template>
  <div>
    <h3>Componente Info</h3>
    <p v-if="esta_trabalhando"><strong>Status:</strong> Estou trabalhando nesse momento</p>
    <p v-else>Buscando oportunidades</p>

    <div v-show="mostrar_tecnologias">
      <h3>Tecnologias Backend</h3>
      <p>Utilizo as seguintes tecnologias para backend:</p>
      <ul>
        <li v-for="(tec, index) in backend_tecs" :key="index">{{ tec }}</li>
      </ul>

      <h3>Tecnologias Frontend</h3>
      <p>Utilizo as seguintes tecnologias para backend:</p>
      <ul>
        <li v-for="frontend in frontend_tecs" :key="frontend.id">{{ frontend.name }}</li>
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
      backend_tecs: ['JavaScript', 'PHP', 'HTML'],
      frontend_tecs: [
        {id: 1, name: 'Vue.js'},
        {id: 2, name: 'React.js'},
        {id: 3, name: 'Angular'},
      ],
    };
  },
};
</script>
