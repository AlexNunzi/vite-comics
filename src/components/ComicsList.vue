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
                <img class="comic-img mb-2" :src="comic.thumb" :alt="comic.series">
                <h4 class="fs-075">{{ comic.series }}</h4>
            </li>
        </ul>

        <button class="load-btn text-white bg-tag d-block m-auto fw-bold">LOAD MORE</button>
    </div>
</template>

<style scoped>
.jumbotron{
    height: 25rem;
    background-image: url(/jumbotron.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    background-position-y: 0px;
}

.comic-img{
    height: 11rem;
    width: 11rem;
    object-fit: cover;
    object-position: top;
}

.comic-card{
    width: calc(100% / 6);
    padding: 1rem;
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
}

#cards{
    position: relative;
}
</style>