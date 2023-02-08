<template>
  <div class="door" :class="{ open }">
    <Gift v-if="hasGift && open" />
    <div class="number">{{ number }}</div>
    <div class="knob" @click="open = true"></div>
  </div>
</template>

<script>
import Gift from "./Gift.vue";
export default {
  name: "Door-componente",
  props: {
    hasGift: Boolean,
    number: {},
  },
  components: { Gift },
  data() {
    return {
      open: false,
    };
  },
};
</script>

<style>
.door {
  position: relative;
  width: 150px;
  height: 250px;
  background-color: rgb(216, 87, 87);
  display: flex;
  border-top: 10px solid brown;
  border-right: 10px solid brown;
  border-left: 10px solid brown;
  border-bottom: 10px solid grey;
  margin: 20px;
  top: 40px;
  flex-wrap: wrap;
}

.knob {
  position: absolute;
  display: flex;
  flex-direction: column;
  width: 20px;
  height: 20px;
  background-color: brown;
  border-radius: 50%;
  margin: 10px;
  justify-content: start;
  /* align-items: center; */
  top: 90px;
}

.door.open {
  background-color: transparent;
  justify-content: center;
}

.door.open .knob,
.door.open .number {
  display: none;
}

.door .number {
  font-size: 30px;
  color: white;
  display: flex;
  align-items: center;
  justify-items: center;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  margin-top: 10px;
}
</style>