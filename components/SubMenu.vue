<template>
<header class="main-header">
    <nav class="main-nav">
        <ul class="nav-links">
            <nuxt-link to="/blog" tag="li" class="nav-link"><a>latest |</a></nuxt-link>
            <nuxt-link to="/about" tag="li" class="nav-link"><a>news |</a></nuxt-link>
            <nuxt-link to="/about" tag="li" class="nav-link"><a>All Posts |</a></nuxt-link>
            <nuxt-link to="/about" tag="li" class="nav-link"><a>burgers |</a></nuxt-link>
            <nuxt-link to="/about" tag="li" class="nav-link"><a>desserts |</a></nuxt-link>
            <nuxt-link to="/about" tag="li" class="nav-link"><a>boissons |</a></nuxt-link>
            <nuxt-link to="/about" tag="li" class="nav-link"><a>about |</a></nuxt-link>
        </ul>
    </nav>
</header>
</template>

<style scoped>

.main-header{
  /*  margin-top: 50px; */
    position: relative;
    width: 100%;
    height: 3.5rem;
}
.main-nav{
    height: 100%;
}
.nav-links{
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
}

.nav-link{
    display:flex;
    justify-content: center;
    align-items: center;
    margin: 0 1rem;
    padding: 0.3rem;
    height: 100%; 
    
}
.nav-link a{
    display: block;
    text-decoration: none;
    color: #A0A0A0;
    margin: 1rem;
}
.nav-link a:hover,
.nav-link a:active,
.nav-link.nuxt-link-active a{
    color:#00A000;
}

</style>

