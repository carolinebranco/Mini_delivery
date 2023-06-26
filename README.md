# Mini_delivery
mini delivery 
carol projetos
<template>
  <div>
    <h2>Produtos Disponíveis</h2>
    <ul>
      <li v-for="produto in produtos" :key="produto.id">
        {{ produto.nome }} - R$ {{ produto.preco }}
        <button @click="adicionarAoCarrinho(produto)">Adicionar ao Carrinho</button>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      produtos: [
        { id: 1, nome: 'Erva 1', preco: 10 },
        { id: 2, nome: 'Erva 2', preco: 15 },
        { id: 3, nome: 'Erva 3', preco: 20 }
      ]
    };
  },
  methods: {
    adicionarAoCarrinho(produto) {
      this.$store.commit('adicionarAoCarrinho', produto);
    }
  }
};
</script>
