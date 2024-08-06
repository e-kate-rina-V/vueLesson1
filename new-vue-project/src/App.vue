<template>
  <div>
    <header>
      <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
      <div class="wrapper">
        <HelloWorld msg="You did it!" />
      </div>
    </header>

    <main>
      <h1>{{ message }}</h1>
      <!-- Передача message як пропс до secondary-comp -->
      <secondary-comp :parentMessage="message" />
      <Placeholder />
    </main>
  </div>
</template>

<script>
import { defineComponent, defineAsyncComponent } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import Placeholder from './components/Placeholder.vue';

const SecondaryComp = defineAsyncComponent(() => import('./components/SecondaryComp.vue'));

export default defineComponent({
  name: 'App',
  components: {
    HelloWorld,
    Placeholder,
    'secondary-comp': SecondaryComp
  },
  data() {
    return {
      message: 'Hello from the main component!'
    };
  }
});
</script>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}

main {
  padding: 1rem;
}

h1 {
  margin-bottom: 1rem;
}
</style>
