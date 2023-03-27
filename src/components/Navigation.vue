<script>
    export default{
        name: 'Navigation',
        data(){
            return {
                footerBottomLinks: [
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
                    icon: 'buy-dc-power-visa.png'
                }
            ]
            }
        }
    }
</script>

<template>

<div class="navigation-container">

</div>

</template>

<style lang="scss">
@use "../styles/variables";

    .navigation-container{
        background-color: variables.$secondary-color;
        height: 160px;
    }

</style>