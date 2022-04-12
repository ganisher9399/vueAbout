<template>
    <div class="btn-block">
        <the-button @action ="setIndex"/>
    </div>
</template>


<script>

import theButton from '../components/The-button.vue'

export default {
    components: {
      theButton
    },
    methods: {
        setIndex(idx){
           this.$emit('action', idx)
        }
    }
}
</script>


<style lang="scss">
   .btn-block{
       display: flex;
       justify-content: center;
       margin: 100px 0 120px;

   } 
</style>