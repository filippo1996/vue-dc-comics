<template>
    <section class="current-series">
        <div class="container">
            <div class="category">{{ nameCategory }}</div>
            <div class="row">
                <div class="col-2" v-for="(product, index) in products" :key="index">
                    <CardProduct :thumb="product.thumb" :series="product.series"/>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import CardProduct from './CardProduct.vue';

export default {

    name: 'GridProduct',
    props: {
        nameCategory: String,
        products: Array
    },
    components: {
        CardProduct
    }
}
</script>

<style scoped lang="scss">
@import '@/style/vars.scss';

.current-series{
    background: $colorPrimary;
    padding: 30px 0;
    position: relative;
}

.category{
    display: inline-block;
    color: white;
    text-transform: uppercase;
    background: $colorSecondary;
    padding: 10px;
    position: absolute;
    top: -23px;
}
</style>