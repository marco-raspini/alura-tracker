<template>
    <section>
        <strong> {{ tempoDecorrido }} </strong>
    </section>
</template>

<script>

    import { defineComponent } from 'vue'

    export default defineComponent({
        name : 'StopWatch',

        propertys: {
            tempoEmSegundos: {
                type: Number,
                default: 0
            }
        },
        computed: {
            tempoDecorrido () : string {
                return new Date(this.tempoEmSegundos * 1000).toISOString().substr(11,8)
            }
        },

})

</script>