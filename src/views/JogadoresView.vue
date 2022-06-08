<script>
export default {
  data() {
    return {
      jogadores: [
        { id: 1, name: "Time 1", nomes: "jogador1", actions: "ação1" },
        { id: 2, name: "Time 2", nomes: "jogador2", actions: "ação2" },
        { id: 3, name: "Time 3", nomes: "jogador3", actions: "ação3" },
        { id: 4, name: "Time 4", nomes: "jogador4", actions: "ação4" },
      ],
    };
  },
};
</script>
<template>
  <div class="container">
    <div class="title">
      <h2>Gerenciamento de jogadores</h2>
    </div>
  </div>
  <div class="form-input">
    <input type="text" placeholder="Insira os nomes" />
    <button>Salvar</button>
  </div>
  <div class="list-items">
    <table>
      <thead>
        <tr>
          <th>ID</th>
          <th>Time</th>
          <th>Nome</th>
          <th>Ações</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="jogador in jogadores" :key="jogador.id">
          <td>{{ jogador.id }}</td>
          <td>{{ jogador.name }}</td>
          <td>{{ jogador.nomes }}</td>
          <td>{{ jogador.actions }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
