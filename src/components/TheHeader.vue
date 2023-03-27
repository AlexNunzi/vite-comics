<script>

export default{
    name: 'TheHeader',
}

</script>

<template>
    <header>
        <div id="head" class="container d-flex justify-content-between align-center h-100">
            <img id="logo" src="/dc-logo.png" alt="DC logo">
            <nav class="h-100">
                <ul class="list-style-none h-100 d-flex align-center">
                    <li class="navLinkContainer">
                        <a class="p-3 text-decoration-none primary-text-color" href="#">Link</a>
                    </li>
                    <li class="navLinkContainer selected-link">
                        <a class="p-3 text-decoration-none primary-text-color" href="#">Link</a>
                    </li>
                    <li class="navLinkContainer">
                        <a class="p-3 text-decoration-none primary-text-color" href="#">Link</a>
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
    }
</style>
