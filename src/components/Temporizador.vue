<template>
    <div class="is-flex is-align-items-center is-justify-content-space-around">
        <StopWatch/>
        <button class="button" @click="iniciar">
            <span class="icon">
                <i class="fas fa-play"></i>
            </span>
            <span>play</span>
        </button>

        <button class="button" @click="finalizar">
            <span class="icon">
                <i class="fas fa-stop"></i>
            </span>
            <span>stop</span>
        </button>
    </div>
</template>

<script lang="ts">

    import { defineComponent } from 'vue';
    import StopWatch from './Cronometro.vue';


    export default defineComponent({
        name: 'TimerClock',

        components: {
            StopWatch,
        },
        data() {
            return {
                tempoEmSegundos: 0,
                cronometro: 0
            }
        },

        methods: {
            // Começar a contagem
            iniciar() {
                this.cronometro = setInterval(() => { this.tempoEmSegundos += 1}, 1000),
                console.log('Iniciando')
            },
            // Finalizar a contagem
            finalizar() {
                clearInterval(this.cronometro)
            }
        }

    })

</script>