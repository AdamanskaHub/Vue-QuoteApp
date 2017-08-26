<template>


      <div class="row">
        <form action="">
           <div class="col-sm-8 col-sm-offset-2 col-md-6 ">
               <label>Quote</label>
               <textarea class="form-control" rows="3" v-model="quote"></textarea>
           </div>
           <div class="col-sm-8 col-sm-offset-2 col-md-6 ">
               <button class="btn btn-primary" @click="createNew">Add a quote</button>
           </div>
        </form>
      </div>

</template>

<script>

    export default {
        data: function() {
            return{
                quote: '', // pour text area
            };
        }
    }


</script>

<style scoped>

</style>
