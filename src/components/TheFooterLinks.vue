<script>

export default{
    name: 'FooterLinks',
    data(){
        return{
            footerLinks: [
                {
                    heading: 'dc comics',
                    links: [
                        {
                            href: '#characters',
                            text: 'Characters'
                        },
                        {
                            href: '#comics',
                            text: 'Comics'
                        },
                        {
                            href: '#movie',
                            text: 'Movie'
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
                            href: '#videos',
                            text: 'Videos'
                        },
                        {
                            href: '#news',
                            text: 'News'
                        }
                    ]
                },
                {
                    heading: 'shop',
                    links: [
                        {
                            href: '#shopDc',
                            text: 'Shop DC'
                        },
                        {
                            href: '#collectibles',
                            text: 'Shop DC Collectibles'
                        }
                    ]
                },
                {
                    heading: 'dc',
                    links: [
                        {
                            href: '#termofuse',
                            text: 'Term Of Use'
                        },
                        {
                            href: '#privacy',
                            text: 'Privacy policy (new)'
                        },
                        {
                            href: '#adChoices',
                            text: 'Ad Choices'
                        },
                        {
                            href: '#adv',
                            text: 'Advertaising'
                        },
                        {
                            href: '#jobs',
                            text: 'Jobs'
                        },
                        {
                            href: '#subscriptions',
                            text: 'Subscriptions'
                        },
                        {
                            href: '#workshops',
                            text: 'Talent Workshops'
                        },
                        {
                            href: '#cpsc',
                            text: 'CPS Certificates'
                        },
                        {
                            href: '#ratings',
                            text: 'Ratings'
                        },
                        {
                            href: '#help',
                            text: 'Shop Help'
                        },
                        {
                            href: '#contact',
                            text: 'Contact Us'
                        }
                    ]
                },
                {
                    heading: 'sites',
                    links: [
                        {
                            href: '#dc',
                            text: 'DC'
                        },
                        {
                            href: '#madMagazine',
                            text: 'MAD Magazine'
                        },
                        {
                            href: '#dcKids',
                            text: 'DC Kids'
                        },
                        {
                            href: '#dcUniverse',
                            text: 'DC Universe'
                        },
                        {
                            href: '#dcPowerVisa',
                            text: 'DC Pover Visa'
                        }
                    ]
                }

            ],
            footerBottomLinks: [
                {
                    text: 'Periscope',
                    href: '#facebook',
                    icon: 'footer-facebook.png'
                },
                {
                    text: 'Twitter',
                    href: '#twitter',
                    icon: 'footer-twitter.png'
                },
                {
                    text: 'Youtube',
                    href: '#youtube',
                    icon: 'footer-youtube.png'
                },
                {
                    text: 'Pinterest',
                    href: '#pinterest',
                    icon: 'footer-pinterest.png'
                },
                {
                    text: 'Periscope',
                    href: '#periscope',
                    icon: 'footer-periscope.png'
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

<footer>

    <div id="footer-top">
        <div class="container h-100 d-flex justify-content-between">
            <ul id="footer-links-container" class="list-style-none">
                <ul class="links-list list-style-none" v-for="list in footerLinks">
                    <li>
                        <h3 class="links-head text-white">{{ list.heading.toUpperCase() }}</h3>
                    </li>
                    <li v-for="link in list.links">
                        <a class="text-decoration-none terthiary-text-color fs-075" href="#">{{ link.text }}</a>
                    </li>
                </ul>
            </ul>

            <div class="transparent-logo h-100"></div>
        </div>
    </div>

    <div id="footer-bottom">
        <div class="container h-100 d-flex justify-content-between align-center">
            <a id="signUpBtn" class="text-white text-decoration-none" href="#">SIGN UP NOW!</a>
            <ul class="d-flex align-center list-style-none">
                <li class="m-3">
                    <h3 class="secondary-text-color">FOLLOW US</h3>
                </li>
                <li v-for="link in footerBottomLinks" class="m-2">
                    <a :href="link.href">
                        <img :src="getImagePath(link.icon)" :alt="link.text">
                    </a>
                </li>
            </ul>
        </div>
        
        
    </div>
</footer>

</template>

<style>
#footer-top{
    height: 20rem;
    background-image: url(/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;
}

.transparent-logo{
    background-image: url(/dc-logo-bg.png);
    background-position: center;
    width: 500px;
    background-repeat: no-repeat;
    background-size: cover;
}

#footer-links-container{
    padding: 1rem 1rem 0 0;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
}

.links-head{
    margin-bottom: 0.5rem;
    margin-top: 1rem;
}

.links-list {
    margin-right: 1.5rem;
}

#footer-bottom{
    height: 7.5rem;
    background-color: var(--footer-bottom-bg);
}

#signUpBtn{
    padding: 1rem;
    border: 2px solid var(--secondary-color);
}
</style>