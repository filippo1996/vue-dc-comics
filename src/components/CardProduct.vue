<template>
    <div class="content">
        <div class="card">
            <img :src="thumb" :alt="series">
        </div>
        <p class="title">{{series}}</p>
    </div>
</template>

<script>
export default {
    name: 'CardProduct',
    props: {
        thumb: String,
        series: String
    }
}
</script>

<style scoped lang="scss">
.content{
    margin-right: 20px;
    margin-bottom: 20px;
    cursor: pointer;
}

.card{
    height: 160px;
    overflow: hidden;
    
    img{
        width: 100%;
    }
}

.title{
    color: white;
    text-transform: uppercase;
    margin-top: 10px;
}
</style>