//Завдання 9: Створіть другорядний об'єкт Vue і прив'яжіть його до деякого елементу HTML на вашій сторінці.

//Завдання 10: Передайте данні від основного об'єкта до другорядного.

<template>
  <div>
    <p>Message from parent: {{ parentMessage }}</p>
  </div>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'SecondaryComp',
  props: {
    parentMessage: {
      type: String,
      required: true
    }
  }
});
</script>

<style scoped>

</style>
