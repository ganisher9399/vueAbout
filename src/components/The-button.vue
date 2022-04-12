<template >
  <div>
    <button class="btn" 
    v-for="(btn, idx) in btnInfo" 
    :key="btn.btnName"
    :class="{active: activeBtn === idx}"
    @click="setActive(idx)"
   

    >
        {{ btn.btnName }}
   </button>
  </div>
</template>
<script>



export default {
   inject: ['btnInfo'],
   data(){
       return {
           activeBtn: 0
       }
   },
   methods: {
       setActive(idx){
           this.activeBtn = idx,
           this.$emit('action', idx)
       }
   }


}
</script>
<style lang="scss">
    .btn{
        padding: 20px 30px;
        margin: 15px;
        text-transform: uppercase;
        letter-spacing: 2px;
        background: transparent;
        color: #fff;
        border-radius: 10px;
        transition: 0.5s;
        border: #fff 1px solid;

        &:hover{
            box-shadow: 0px 10px 20px #15007b;
        }
    }
    .active{
        background: rgb(7, 0, 148);
    }
</style>