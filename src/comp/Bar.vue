<template>
    <div>
        <h3 v-if="quotesIn">Quote added</h3>
        <h3 v-else>Quote counter</h3>
        <div class="bar" v-bind:style="chargedBar"></div>
    </div>
</template>

<script>
    export default {
        data: function() {
            return {
                quotesIn: false,
                // chargedBar: {
                //     backgroundColor: 'green',
                //     margin: 0,
                //     color: 'white',
                //     width: '0%',
                // },
            };
        },
        methods: {
            init: function(){
            this.chargedBar.width = '0%';
            this.chargedBar.backgroundColor = 'green';
            }
        }
        
    }
</script>

<style scoped>
    .bar {
    width: 80%;
    height: 20px;
    border-radius: 10px;
    background-color: #eee;
    margin: auto;
    transition: width 500ms;
}
</style>
