<template>


      <div class="col-md-4">
          <div class="panel panel-default">
              <div class="panel-body quote">
                  <slot></slot>
              </div>
          </div>
      </div>


</template>

<script>

    // export default {
    //     props: ['quotesX'],
    // }


</script>

<style scoped>
    .panel-body {
        font-family: cursive;
    }
    .quote {
        cursor: pointer;
    }
    .quote:hover {
        background-color: red;
    }
</style>
