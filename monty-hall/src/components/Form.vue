<template>
  <div class="form">
    <div v-if="!start">
      <label for="portas">Quantas portas?</label>
      <input type="number" id="portas" size="2" v-model.number="portas" />
    </div>
    <div v-if="!start">
      <label>Qual porta sorteada?</label>
      <input
        type="number"
        id="sorteada"
        size="2"
        v-model.number="portaSelecionada"
      />
    </div>
    <button v-if="!start" @click="start = true">Enviar</button>
    <button v-if="start" @click="start = false">Reiniciar</button>
    <div class="doorSelect" v-if="start">
      <div v-for="i in portas" :key="i">
        <Door :hasGift="i == portaSelecionada" :number="i" />
      </div>
    </div>
  </div>
</template>

<script>
import Door from "./Door.vue";

export default {
  name: "MyForm",
  components: { Door },
  data() {
    return {
      start: false,
      portas: 3,
      portaSelecionada: null,
    };
  },
};
</script>

<style>
.form {
  color: #000;
  width: 300px;
  height: 200px;

  align-items: center;
  margin: 10px;
  flex-direction: row;
}

#portas,
#sorteada {
  flex-direction: column;
  width: 30px;
  margin-left: 10px;
  flex-wrap: wrap;
  justify-content: flex-start;
  margin-top: 10px;
}

button {
  margin-top: 10px;
  background-color: pink;
  border: none;
  width: 80px;
  height: 30px;
  border-radius: 10%;
}

.doorSelect {
  display: flex;
  justify-content: stretch;
  margin: 10px;
  padding: 20px;
  flex-wrap: wrap;
}

input[type="number"]::-webkit-inner-spin-button,
input[type="number"]::-webkit-outer-spin-button {
  -webkit-appearance: none;
  margin: 0;
}
</style>