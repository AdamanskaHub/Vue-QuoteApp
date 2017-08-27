<template>


      <div class="row">
          <app-quote v-for="(item, index) in quotes" @click.native="deleteQuote(index)"> {{ item }}</app-quote>
          <!-- je dois retourner dans app.vue et écouter l'event delete, là où j'appelle app-block -->
           <!-- native semble faire que ça s'applique à tout le component comme zone de click-->
    
      </div>


</template>

<script>
    import Quote from './Quote.vue';

    export default {
        props: ['quotes'],
        components: {
            appQuote: Quote,
        },
        methods: {
            deleteQuote(theIndex) {
                this.$emit("quoteDeleted", theIndex);
            }
        }
    }


</script>

<style scoped>
    .box {
        width: 23%;
        margin-right: 2%;
        border: 1px #ccc solid;
    }
</style>
