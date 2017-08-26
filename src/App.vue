<template>
    <div class="container">
        <app-bar></app-bar>
        <app-txt></app-txt>
        <app-block></app-block>
    </div>
</template>

<script>
    import Bar from './comp/Bar.vue';
    import Txt from './comp/Txt.vue';
    import Block from './comp/Block.vue';

    export default {
        data: function () {
            return {
                quoteTitle: "Title passed in data",
                // selectedComponent: 'app-quote', // appQuote - c'est la valeure défaut
            }
        },
        components: {
            appBar: Bar, // nécessaire pour passer app-quote ici
            appTxt:Txt,
            appBlock: Block,
        }
    }
</script>

<style>
</style>
