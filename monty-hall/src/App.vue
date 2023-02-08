<template>
  <Form/>
</template>

<script>
import Form from "./components/Form.vue";


export default {
  name: "App",
  components: {
    Form
  },
};
</script>

<style>

body {
  background: linear-gradient(to right, rgb(141, 86, 95), rgb(255, 64, 96));

}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  justify-content: center;
}
</style>
