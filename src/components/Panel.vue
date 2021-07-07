<template>
    <section>
        <div class="container">
            <div class="panel">
                <div v-for="(icon, index) in icons" :key="index" class="icon">
                    <img :src="icon.imgPath" :alt="icon.alt">
                    <span class="text-ico">{{ icon.title }}</span>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Panel',
    data(){
        return {
            icons: [
                {
                    imgPath: require('../assets/img/buy-comics-digital-comics.png'),
                    alt: 'Digital Comics',
                    title: 'Digital Comics'
                },
                {
                    imgPath: require('../assets/img/buy-comics-merchandise.png'),
                    alt: 'DC Merchandise',
                    title: 'DC Merchandise'
                },
                {
                    imgPath: require('../assets/img/buy-comics-subscriptions.png'),
                    alt: 'Subscription',
                    title: 'Subscription'
                },
                {
                    imgPath: require('../assets/img/buy-comics-shop-locator.png'),
                    alt: 'locator',
                    title: 'Comic shop locator'
                },
                {
                    imgPath: require('../assets/img/buy-dc-power-visa.svg'),
                    alt: 'Visa card',
                    title: 'Dc power visa'
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';

section{
    background: $colorSecondary;
    padding: 25px;
}

.panel{
    display: flex;
    justify-content: space-around;
    align-items: center;
}

.icon{

    img{
        width: 45px;
        vertical-align: middle;
    }
}

.text-ico{
    margin-left: 20px;
    text-transform: uppercase;
    color: white;
    font-size: .8rem;
}
</style>