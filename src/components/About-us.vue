<template>
    <div class="wrapper">
        <div class="banner"> 
            <img :src="img" alt="redmi 10s">
        </div>
        <div class="content">
                <h1>{{ title }}</h1>
                <p>{{ text }}</p>
        </div>
    </div>
</template>


<script>
export default {
    data() {
        return {
            img: 'https://avatars.mds.yandex.net/get-marketcms/1779479/img-9bc8b921-8cc4-4cd8-a311-2e7623731eac.jpeg/optimize',
            title: 'Hwllo Title',
            text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Repellendus rem impedit veniam rerum mollitia, modi magni eaque et explicabo obcaecati repellat nihil quos nemo, saepe soluta quis dicta voluptatibus delectus?'

        }
    },
}
</script>


<style lang="scss" scoped>
   .wrapper {
       display: flex;
       justify-content: space-between;
       align-items: center;
   } 
   .banner,
   .content {
       width: 47%;

   }

   img{
       width: 100%;
       min-height:400px;
       background-size: cover;
       background-position: center;
       background-repeat: no-repeat;
   }
</style>