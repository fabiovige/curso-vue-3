<template>
    <img :src="url" :alt="title">
    <MudarImagem @mudarImagem="trocarImagem"/>
</template>

<script>
import MudarImagem from './MudarImagem.vue';
export default {
    name: 'PictureInfo',
    components: {
        MudarImagem
    },
    data() {
        return {
            url: 'https://via.placeholder.com/150',
            title: 'A picture'
        }
    },
    methods: {
        trocarImagem() {
            console.log('Imagem trocada');
            this.url = 'https://via.placeholder.com/150/0000FF/808080?Text=Digital.com';
        }
    }
}
</script>