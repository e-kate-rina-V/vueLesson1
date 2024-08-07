<template>
<div>
<!--Завдання 6: Створіть форму вводу тексту та зв'яжіть введене значення з властивістю об'єкта Vue. 
Виведіть введений текст на сторінці.-->
 <input class v-model="text" placeholder="Enter some text" />
    <label class ="textlabel">{{ text }}</label>
     <event-handler/>
</div>
</template>

<script>
//Завдання 7: Створіть ще один окремий файл з компонентом, зареєструйте та 
//використуйте його у існуючему компоненті.

import EventHandler from './EventHandler.vue';

export default {
    name: 'Placeholder', 
    components: {
    EventHandler
  },
    data() {
        return {
            text: ''
        }
    }
}
</script>

<style scoped>
.textlabel {
    margin-left: 5%;
}
</style>
