<template>
    <div class="row">
        <quote v-for="(quote,index) in quotes" :key="quote" @click.native="removeQuote(index)"> {{quote}} </quote>
    </div>
</template>

<script>
import Quote from './Quote.vue'

export default {
    name: 'QuoteGrid',
    components: {Quote},
    props: {
        quotes: {type: Array, required: true}
    },
    methods: {
        removeQuote(index) {
            this.quotes.splice(index, 1)
        }
    },
}
</script>
