<template>
    <div class="box">
        <div class="columns">
            <div class="column is-8" role="form" aria-label="Formulário para criação de uma nova tarefa">
                <input type="text" class="input" placeholder="Qual tarefa você deseja iniciar?"/>
            </div>

            <div class="column">
                <TimerClock/>
            </div>
        </div>
    </div>
</template>

<script lang="ts">

    import { defineComponent } from 'vue';
    import TimerClock from './Temporizador.vue';


    export default defineComponent({
        name: 'FormText',

        components: {
            TimerClock,
        }
    });

</script>

<style>


</style>