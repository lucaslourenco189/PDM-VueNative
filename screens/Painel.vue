<template>
  <view class="container">
    <status-bar background-color="black" bar-style="light-content" />
    <text class="text-recuperar">Seja bem vindo!</text>
    <view class="itens">
      <button
        class="btn-entrar"
        title="Meus dados"
        color="black"
        @press="changeRoute"
      ></button>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      email: "E-mail",
      senha: "Senha",
    };
  },
  props: {
    navigation: { type: Object },
  },
  methods: {
    pressionar: function () {
      alert("Olá, usuário!");
    },
    changeRoute() {
      this.navigation.navigate("Details");
    },
  },
};
</script>

<style>
.container {
  background-color: white;
  align-items: center;
  display: flex;
}

.itens {
  display: flex;
}

.label {
  align-self: flex-start;
}
.text-recuperar {
  margin: 10%;
  font-size: 40px;
  color: black;
}

.input {
  width: 98%;
  margin: 10px 10px;
  border-radius: 1px;
  padding: 10px;
  border-width: 1;
}
</style>
