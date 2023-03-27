<script>

export default{
    name: 'TheHeader',
    data(){
        return{
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
                    <li v-for="link in navLinks" class="navLinkContainer">
                        <a class="p-3 text-decoration-none primary-text-color" :href="link.href">{{ link.text.toUpperCase() }}</a>
                    </li>
                </ul>
            </nav>

        </div>
    </header>

</template>

<style scoped>
    header{
        height: 120px;
    }

    #logo{
        height: 80px;
    }

    .navLinkContainer{
        line-height: 120px;
        height: 100%;
    }

    .selected-link{
        border-bottom: 5px solid var(--secondary-color);
    }

    .selected-link a{
        color: var(--secondary-color);
        font-weight: bold;
        font-size: 0.75rem;
    }
</style>
