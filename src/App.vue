<template>
    <div class="container">
        <app-bar></app-bar>
        <app-txt></app-txt>
        <app-block :quotes="quotes"></app-block>
    </div>
</template>

<script>

    import { Bus } from './main.js';

    import Bar from './comp/Bar.vue';
    import Txt from './comp/Txt.vue';
    import Block from './comp/Block.vue';
    import Quote from './comp/Quote.vue';

    export default {
        data: function () {
            return {
                quotes: ['gnej jcekrvn jk jjhkjb jjoefjov'],
                maxQuotes: 10,
            }
        },
        components: {
            appBar: Bar, // nécessaire pour passer app-quote ici
            appTxt:Txt,
            appBlock: Block,
            appQuote: Quote,
        }
    }
</script>

<style>
</style>
