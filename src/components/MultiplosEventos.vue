<template>
  <div>
    <h2>Multiplos Eventos</h2>
    <button :disabled="bloqueado" @click="primeiro(txt1), segundo(txt2)">
      Ativa multiplos eventos {{ count }}
    </button>
    <p>{{ multiplos_eventos }}</p>
    <p>{{ count }}</p>
  </div>
</template>
<script>
export default {
  name: 'MultiplosEventos',
  data() {
    return {
      multiplos_eventos: '',
      count: 0,
      interval: null,
      bloqueado: false,
      txt1: 'Primeiro evento',
      txt2: 'Segundo evento',
    };
  },
  methods: {
    primeiro(txt) {
      this.multiplos_eventos = 'Multiplos eventos ativados ' + txt;
    },
    segundo(txt) {
      this.interval = setInterval(() => {
        this.count++;
        console.log(this.count);
        if (this.count === 5) {
          this.multiplos_eventos = 'Multiplos eventos desativados ' + txt;
          this.bloqueado = true;
          clearInterval(this.interval);
        }
      }, 1000);
    },
  },
};
</script>
<style scoped>
div {
  margin: 20px;
}
</style>