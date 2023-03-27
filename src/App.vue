<script>

import TheHeader from "./components/TheHeader.vue";
import Navigation from"./components/Navigation.vue";
export default{
  components:{
    TheHeader,
    Navigation,
  }
}
</script>

<template>

<TheHeader />

<main>
  <div class="main-content container d-flex align-center">
    <h1>Content goes hear</h1>
  </div>
</main>

<Navigation />

</template>

<style>
:root{
  --primary-color: #000000;
  --secondary-color: #0082F9;
}

.primary-text-color{
  color: var(--primary-color);
}

.container{
  margin: 0 auto;
  max-width: 1170px;
}

.d-flex{
  display: flex;
}

.justify-content-between{
  justify-content: space-between;
}

.align-center{
  align-items: center;
}

.h-100{
  height: 100%;
}

.list-style-none{
  list-style: none;
}

.text-decoration-none{
  text-decoration: none;
}

.d-block{
  display: block;
}

.d-inline-block{
  display: inline-block;
}

.p-3{
  padding: 1rem;
}

main{
  background-color: black;
}

.main-content{
  height: 200px;
  color: #FFFFFF;
}

</style>
