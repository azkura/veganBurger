<template>
<header class="main-header">
    <nav class="main-nav">
        <ul class="nav-links">
            <nuxt-link to="/blog" tag="li" class="nav-link"><a>Suscribe</a></nuxt-link>
            <nuxt-link to="/about" tag="li" class="nav-link-home"><a>vegan | Fast</a></nuxt-link>
             <nuxt-link to="/about" tag="li" ><button> <font-awesome-icon icon="search" /></button></nuxt-link>
            <nuxt-link to="/about" tag="li" class="nav-link"><button>sign up</button></nuxt-link>
           
        </ul>
    </nav>
</header>
</template>

<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { faSearch } from '@fortawesome/free-solid-svg-icons'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
library.add(faSearch)

export default {
    components:{
        FontAwesomeIcon
    },
}
</script>

<style scoped>
.main-header{
    position:flex;
    background: #fffff0;
    top: 0;
    left: 0;
 /*   left: 4.5rem;
    right: 4.5rem;
    width: 100%; */
    border-bottom: 1px solid #A8A8A8;
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
   
}
.nav-link-home a{
    display: block;
    text-decoration: none;
    color: #00A000;
    font-family: 'Pacifico', cursive;
    font-size: 30px;

}
button{
    background: white;
    color: #A0A0A0;
    border: 1px solid #A0A0A0;
    border-radius: 2px;
}
.nav-link a:hover,
.nav-link a:active,
.nav-link.nuxt-link-active a{
    color:#00A000;
}

</style>

