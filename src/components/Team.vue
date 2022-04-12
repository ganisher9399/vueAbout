<template>
    <div class="wrapper">
        <div class="card" 
        v-for="member in team" :key="member.name">
            <img :src="member.img" alt="">
            <h3> {{ member.name }}</h3>
            <p> {{ member.job }} </p>
        </div>
    </div>
</template>


<script>
export default {
    data() {
        return {
            team: [
                {
                   img: 'https://uznayvse.ru/images/catalog/2022/3/pavel-durov_90.jpg',
                   name: 'Pavel Durov',
                   job: 'Telegram asoschisi', 
                },
                {
                   img: 'https://phantom-marca.unidadeditorial.es/62c97a5a219864d3b9abef11c142b18d/resize/1320/f/jpg/assets/multimedia/imagenes/2021/10/05/16334175825288.jpg',
                   name: 'mark zuckerberg',
                   job: 'Facebook asoschisi', 
                },
                {
                   img: 'https://hs-marketing.imgix.net/images/blog/steve-jobs.jpg?ixlib=gatsbyHook-1.7.0&fit=min&auto=format%2Ccompress&placeholder=dominantColor&w=610&h=343',
                   name: 'Steve Jobs',
                   job: 'Apple asoschisi', 
                },
                {
                   img: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQXDHs_Tnl0wWQy2qvPY9GPPqmfJpsDpXIbww&usqp=CAU',
                   name: 'Jeck ma',
                   job: 'biznesmen eng boy odam', 
                },                                                
            ]
        }
    }
}
</script>


<style lang="scss" scoped>
    .wrapper {
        display: flex;
        justify-content: space-between;
    }
    .card {
        width: 250px;
        background: hsla(0, 100%, 54%, 0.171);
        padding: 10px;
        border-radius: 5px;
        img{
            width: 100%;
            height: 300px;
            object-fit: cover;
        }
        h3{
            font-size: 30px;
            margin: 15px 0;
        }
        p{
            color: aqua;
        }
    }
</style>