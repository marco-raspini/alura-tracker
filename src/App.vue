<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
      <SideBar/>
    </div>

    <div class="column is-trhee-quarter">
      <FomrText/>
    </div>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import SideBar from '../src/components/BarraLateral.vue';
import FomrText from '../src/components/Formulario.vue';

export default defineComponent({
  name: 'App',
  components: {
    SideBar,
    FomrText,
  }
});
</script>

<style>

</style>
