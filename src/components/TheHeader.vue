<script>

export default{
    name: 'TheHeader',
    data(){
        return{
            selectedLink: 0,
            navLinks: [
                {
                    href: '#characters',
                    text: 'Characters'
                },
                {
                    href: '#comics',
                    text: 'Comics'
                },
                {
                    href: '#movies',
                    text: 'Movies'
                },
                {
                    href: '#tv',
                    text: 'Tv'
                },
                {
                    href: '#games',
                    text: 'Games'
                },
                {
                    href: '#collectibles',
                    text: 'Collectibles'
                },
                {
                    href: '#videos',
                    text: 'Videos'
                },
                {
                    href: '#fans',
                    text: 'Fans'
                },
                {
                    href: '#news',
                    text: 'News'
                },
                {
                    href: '#shop',
                    text: 'Shop'
                }
            ]
        }
    }
}

</script>

<template>
    <header>
        <div id="head" class="container d-flex justify-content-between align-center h-100">
            <img id="logo" src="/dc-logo.png" alt="DC logo">
            <nav class="h-100">
                <ul class="list-style-none h-100 d-flex align-center">
                    <li v-for="(link, i) in navLinks" class="navLinkContainer mes-3" :class="selectedLink == i ? 'selected-link':''">
                        <a class="ptb-05 text-decoration-none primary-text-color" :href="link.href">{{ link.text.toUpperCase() }}</a>
                    </li>
                </ul>
            </nav>

        </div>
    </header>

</template>

<style scoped lang="scss">
    @use "../styles/partials/variables";

    header{
        height: 7.5rem;
    }

    #logo{
        height: 5rem;
    }

    .navLinkContainer{
        line-height: 7.5rem;
        height: 100%;
        font-size: 0.75rem;
    }

    .navLinkContainer:hover:not(.selected-link){
        border-bottom: 5px solid lighten(variables.$secondary-color, 30); 
    }
    .selected-link{
        border-bottom: 5px solid variables.$secondary-color;
    }

    .selected-link a{
        color: variables.$secondary-color;
        font-weight: bold;
    }
</style>
