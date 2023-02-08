<template>
  <div class="gift">
    <div class="gift-tie-1"></div>
    <div class="gift-tie-2"></div>
    <div class="gift-top"></div>
    <div class="gift-body"></div>
  </div>
</template>

<script>
export default {
  name: "Gift-componente",
};
</script>

<style>
.gift {
  position: relative;
  flex-direction: column;
  width: 90px;
  height: 80px;
  display: flex;
  align-items: center;
  z-index: 10;
  top:180px;
  justify-items: center;
  
}

.gift-top {
  position: absolute;
  background-color: rgb(255, 117, 140);
  width: 100px;
  height: 20px;
  display: flex;
  justify-content: flex-start;
}

.gift-body {
  width: 90px;
  height: 70px;
  display: flex;
  background-color: pink;
  justify-content: flex-end;
  
}

.gift-tie-1 {
  position: absolute;
  background-color: red;
  width: 10px;
  height: 70px;
  display: flex;
  justify-content: center;
  align-items: center;
  align-content: center;
  margin-left: 30;
  z-index: 1;
}

.gift-tie-2 {
  position: absolute;
  top:35px;
  background-color: red;
  width: 90px;
  height: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>