
//Завдання 8: Створіть обробники подій, які реагують на події кліку та змінюють стан вашого об'єкта Vue.

<template>
  <div>
    <h1 :style="{ color: textColor}" @click="changeColor">{{ counter }}</h1>
  </div>
</template>

<script>
export default {
  name: 'EventHandler',
  data() {
    return {
      counter: 'Hello, World!',
      textColor: 'black' 
    };
  },
  methods: {
    changeColor() {
      this.textColor = this.textColor === 'lightblue' ? 'black' : 'lightblue';
    }
  }
};
</script>

<style scoped>
h1 {
  cursor: pointer;
  margin-top: 20px;
  font-size: 25px;
}
</style>
