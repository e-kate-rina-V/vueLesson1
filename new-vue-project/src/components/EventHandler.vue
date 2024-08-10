
<!--Завдання 8: Створіть обробники подій, які реагують на події кліку та змінюють стан вашого об'єкта Vue.-->

<!--Изменение цвета текста при нажатии на него-->

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
      counter: 'Hello!',
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


