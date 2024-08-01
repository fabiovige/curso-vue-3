<template>
  <div>
    <h1>{{ name }}</h1>
    <p>{{ description }}</p>
    <button>Alterar Descrição</button>
  </div>
</template>

<script>
export default {
  name: 'LifeCycle',
  data() {
    return {
      name: 'Exemplo de created e mounted',
      description: 'Desenvolvedor Web',
    };
  },
  created() {
    // Este hook é chamado após a instância do componente ser criada
    console.log('created: O componente foi criado.');
    // Pode ser útil para inicializar dad os ou fazer uma chamada de API

    setTimeout(() => {
      this.initializeComponent();
    }, 1000);
  },
  mounted() {
    // Este hook é chamado após o componente ser montado no DOM
    console.log('mounted: O componente foi montado.');
    // Pode ser útil para manipular o DOM ou fazer configurações baseadas em elementos DOM
    setTimeout(() => {
      this.setupDOMManipulation();
    }, 2000);
  },
  methods: {
    handleClick() {
      this.description = 'Simplicidade e funcionalidades caminham juntos';
    },
    initializeComponent() {
      // Simulação de inicialização de dados ou chamada de API
      console.log('Inicializando componente...');
      // Exemplo: Carregar dados de uma API
      // axios.get('/api/dados').then(response => {
      //   this.data = response.data;
      // });
    },
    setupDOMManipulation() {
      // Simulação de manipulação do DOM
      console.log('Configurando manipulação do DOM...');
      // Exemplo: Adicionar um evento de clique a um elemento DOM
      document.querySelector('button').addEventListener('click', this.handleClick());
      document.querySelector('button').textContent = 'botão clicado no mouted';
    },
  },
};
</script>
