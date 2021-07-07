<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-5 padding">
                    <ul class="d-flex wrap flex-start">
                        <li v-for="(link , index) in links" :key="index" class="title">
                            <h4>{{link.title}}</h4>
                            <ul>
                                <li v-for="(item, index) in link.subTitle" :key="index">
                                    <a class="sub-title" :href="item.url">{{item.text}}</a>
                                </li>
                            </ul>
                        </li>
                    </ul>
                </div>
                <div class="col-7 d-flex justify-content-end">
                    <img class="logo" src="../assets/img/dc-logo-bg.png" alt="logo grande della dc">
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data(){
        return {
            links: [
                {
                    title: 'Dc comics',
                    subTitle: [
                        {
                            text: 'Characters',
                            url: '#'
                        },
                        {
                            text: 'Comics',
                            url: '#'
                        },
                        {
                            text: 'Movies',
                            url: '#'
                        },
                        {
                            text: 'TV',
                            url: '#'
                        },
                        {
                            text: 'Games',
                            url: '#'
                        },
                        {
                            text: 'Videos',
                            url: '#'
                        },
                        {
                            text: 'News',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'Dc',
                    subTitle: [
                        {
                            text: 'Terms Of Use',
                            url: '#'
                        },
                        {
                            text: 'Privacy policy (New)',
                            url: '#'
                        },
                        {
                            text: 'Ad Choices',
                            url: '#'
                        },
                        {
                            text: 'Advertising',
                            url: '#'
                        },
                        {
                            text: 'Jobs',
                            url: '#'
                        },
                        {
                            text: 'Subscriptions',
                            url: '#'
                        },
                        {
                            text: 'Talent Workshops',
                            url: '#'
                        },
                        {
                            text: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            text: 'Ratings',
                            url: '#'
                        },
                        {
                            text: 'Shop Help',
                            url: '#'
                        },
                        {
                            text: 'Contact Us',
                            url: '#'
                        },
                    ]
                },
                {
                    title: 'Sites',
                    subTitle: [
                        {
                            text: 'DC',
                            url: '#'
                        },
                        {
                            text: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            text: 'DC Kids',
                            url: '#'
                        },
                        {
                            text: 'DC Universe',
                            url: '#'
                        },
                        {
                            text: 'DC Power Visa',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'Shop',
                    subTitle: [
                        {
                            text: 'Shop DC',
                            url: '#'
                        },
                        {
                            text: 'Shop DC Colletibles',
                            url: '#'
                        }
                    ]
                }
            ]
        }
    }
}
</script>

<style scoped lang="scss">
footer{
    background: url('../assets/img/footer-bg.jpg');
    height: 482px;
    position: relative;
    overflow: hidden;
}

.logo{
    height: 482px;
    position: absolute;
    top: -85px;
}

.title{
    color: white;
    text-transform: uppercase;
    font-size: 1.4rem;
    font-weight: 800;
    margin-right: 25px;

    h4{
        margin-bottom: 15px;
    }

    .sub-title{
        color: lightgray;
        text-transform: none;
        font-size: .9rem;
        font-weight: 200;
    }
}

.padding{
    padding: 50px 0;
}
</style>