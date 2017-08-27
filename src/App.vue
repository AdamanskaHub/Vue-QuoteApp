<template>
    <div class="container">
        <app-new-quote @quoteAdded = "newQuote"></app-new-quote> 
        <!-- j'écoute pour quoteAdded et je lance si c'est le cas la méthode newQuote -->
        <app-block :quotes="quotes" @quoteDeleted="deleteQuoteX"></app-block>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert">Click box to delete</div>
            </div>
        </div>
        
    </div>
</template>

<script>

    import { Bus } from './main.js';

    import Bar from './comp/Bar.vue';
    import Txt from './comp/Txt.vue';
    import Block from './comp/Block.vue';
    import Quote from './comp/Quote.vue';
    import NewQuote from './comp/NewQuote.vue';

    export default {
        data: function () {
            return {
                quotes: ['gnej jcekrvn jk jjhkjb jjoefjov'],
                maxQuotes: 10,
            }
        },
        methods: {
            newQuote(bla) {
                this.quotes.push(bla);
            },
            deleteQuoteX(indexX) {
                this.quotes.splice(indexX, 1);
            }
        },
        components: {
            appBar: Bar, // nécessaire pour passer app-quote ici
            appTxt:Txt,
            appBlock: Block,
            appQuote: Quote,
            appNewQuote: NewQuote,
        }
    }
</script>

<style>
</style>
