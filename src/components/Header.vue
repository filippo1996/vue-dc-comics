<template>
    <header>
        <div class="container">
            <div class="row">
                <div class="col-2">
                    <a href="#"><img class="logo" src="../assets/img/dc-logo.png" alt="logo DC"></a>
                </div>
                <div class="col-10 d-flex items-center justify-content-end">
                    <ul>
                        <li v-for="(link, index) in links" :key="index"><a :class="link.current ? 'active' : null" :href="link.url">{{link.text}}</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>

<script>
import Links from '@/data/LinksHeader.js';

export default {
    name: 'Header',
    data(){
        return {
            links: Links
        };
    }
}
</script>

<style scoped lang="scss">
@import '../style/vars.scss';

header{
    padding: 15px 0;
}

.logo{
    width: 80px;
}

li{
    display: inline-block;
    margin-right: 20px;

    a{
        text-transform: uppercase;
        color: $colorPrimary;
    }
}

.active{
    color: $colorSecondary;
}
</style>