<script>
export default{
    name: 'ComicsList',
    props: {
        comicsList: Array,
    }
}
</script>

<template>
    <div class="jumbotron"></div>

    <div id="cards" class="container pt-4 pb-3">
        <div id="cards-info" class="d-inline-block text-white fw-bold fs-125 bg-tag">CURRENT SERIES</div>

        <ul class="d-flex flex-wrap list-style-none">
            <li class="comic-card text-white" v-for="(comic, i) in comicsList">
                <a href="#">
                    <img class="mb-2 d-block" :src="comic.thumb" :alt="comic.series">
                </a>
                <h4 class="fs-075">{{ comic.series }}</h4>
            </li>
        </ul>

        <button class="load-btn text-white bg-tag d-block m-auto fw-bold">LOAD MORE</button>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables";
.jumbotron{
    height: 25rem;
    background-image: url(/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-position-y: 0px;
}

.comic-card{
    width: calc(100% / 6);
    padding: 1rem;

    & img{
    height: 11rem;
    width: 11rem;
    object-fit: cover;
    object-position: top;
    }

    & a:hover img{
        transition: 0.25s;
        scale: 1.01;
    }
}

#cards-info{
    padding: 0.75rem 2rem;
    position: absolute;
    top: 0;
    left: 0;
    transform: translateY(-50%);
}
.load-btn{
    padding: 0.75rem 3.5rem;

    &:hover{
        cursor: pointer;
        transition: background-color 0.25s;
        transition: scale 0.25s;
        background-color: lighten(variables.$secondary-color, 5);
        scale: 1.01;
    }

    &:active{
        transition: background-color 0.25s;
        transition: scale 0.25s;
        background-color: darken(variables.$secondary-color, 5);
        scale: 0.99;
    }
}

#cards{
    position: relative;
}
</style>