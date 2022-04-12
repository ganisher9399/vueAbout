<template>
    <div class="wrapper">
        <div class="cert">
            <img 
            v-for="img in certs" 
            :key="img" :src="img" 
            @click="$emit('setModel', img)"
            alt="">
        </div>
    </div>
</template>


<script>
export default {
    data() {
        return {
           certs: [
               'https://www.kaznu.kz/content/images/pages/66703.jpg',
               'https://cdn.create.vista.com/downloads/cd5af41d-d31c-46c0-9a5a-d71617159ea8_450.jpeg',
               'https://cdn.create.vista.com/downloads/e6763e46-d900-424d-ba2d-954031c9703f_450.jpeg',
               'https://santanamed.by/assets/images/1/sertifikat.gif',
           ] 
        }
    }
}
</script>


<style lang="scss" scoped>
    .cert {
        display: flex;
        justify-content: space-between;
        align-items: space-between;
        flex-wrap: wrap;
        gap: 10px;
        

    }
    img {
        width: 49%;
        height: 300px;
        object-fit: cover;
        cursor: pointer;
    }
</style>