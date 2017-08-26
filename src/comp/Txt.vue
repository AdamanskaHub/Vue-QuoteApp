<template>
  <div>
      <p>Quote</p>
      <input v-model="texte" placeholder="Your quote">
      <button @click="add">Add Quote</button>
      <p>{{ texte }}</p>
  </div>
</template>

<script>
export default {
    data: function() {
        return {  
            chargedBarX : 0,
            chargedBar: {
                    backgroundColor: 'green',
                    margin: 0,
                    color: 'white',
                    width: '0%',
                },
            };
    },
    methods: {
        add: function() {
            this.chargedBarX += 10;
            console.log(this.chargedBarX );
            this.chargedBar.width = this.chargedBarX + '%';
            console.log(this.chargedBar.width );
            this.quotesIn = true;
        },
    }
}
</script>

<style scoped>
    
</style>