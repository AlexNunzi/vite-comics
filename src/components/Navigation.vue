<script>
    export default{
        name: 'Navigation',
        data(){
            return {
                navigationLinks: [
                {
                    text: 'Digital Comics',
                    href: '#digitalComics',
                    icon: 'buy-comics-digital-comics.png'
                },
                {
                    text: 'DC Merchandise',
                    href: '#dcMerch',
                    icon: 'buy-comics-merchandise.png'
                },
                {
                    text: 'Subscription',
                    href: '#subscription',
                    icon: 'buy-comics-subscriptions.png'
                },
                {
                    text: 'Comic shop locator',
                    href: '#shopLocation',
                    icon: 'buy-comics-shop-locator.png'
                },
                {
                    text: 'DC power visa',
                    href: '#dcPowerVisa',
                    icon: 'buy-dc-power-visa.svg'
                }
            ]
            }
        },
        methods: {
        getImagePath: function(imageName){
            return new URL(`/public/${imageName}`, import.meta.url).href;
        }
    }
    }
</script>

<template>

<div class="navigation-container d-flex align-center">
    <div class="container pes-5">
        <ul class="list-style-none d-flex align-center justify-content-around flex-wrap">
            <li v-for="(link, i) in navigationLinks" class="navigationCard d-flex align-center">
                <img :src="getImagePath(link.icon)" :alt="link.text" class="icon" :key="`immagine-${i}`" />
                <a :href="link.href" class="fs-075 ms-3 text-decoration-none text-white">{{ link.text.toUpperCase() }}</a>
            </li>
        </ul>
    </div>
</div>

</template>

<style lang="scss">
@use "../styles/partials/variables";

    .navigation-container{
        background-color: variables.$secondary-color;
        height: 160px;
    }

    .icon{
        height: 3.5rem;
        max-width: 3rem;
    }

    .navigationCard{
        width: calc(100% / 5);
    }
</style>