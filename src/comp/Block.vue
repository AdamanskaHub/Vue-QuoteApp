<template>


      <div class="row">
          <app-quote v-for="item in quotes"> {{ item }}</app-quote>
           
    
      </div>


</template>

<script>
    import Quote from './Quote.vue';

    export default {
        props: ['quotes'],
        components: {
            appQuote: Quote,
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
