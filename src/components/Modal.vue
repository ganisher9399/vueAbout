<template>
    <div class="layer" @click="$emit('closeModel')">
        <img :src="imgge" alt="" @click.stop>
    </div>
</template>


<script>
export default {
    props: {
      imgge: String,  
    }
}
</script>


<style lang="scss">
    .layer {
        position: fixed;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        min-width: 100vh;
        background: rgba(0,0,0,0.8);
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: center;
        img{
            width: 70%;
        }
    }

</style>