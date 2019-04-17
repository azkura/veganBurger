<template>
<header class="header">
    <nav class="nav-menu">
        <div class="menu">
            <nuxt-link to=""><a class="home">VEG | HAM </a></nuxt-link>
            <div class="search-container">
                <form>
                    <input type="text" class="input">
                    <button type="submit" class="search"><font-awesome-icon icon="search" /></button>
                </form>
                <nuxt-link to="" class="sign"><button>sign in</button></nuxt-link>
                <nuxt-link to="" class="sign"><button>sign out</button></nuxt-link>
                <nuxt-link to="" class="sign"><button>subscrire</button></nuxt-link>
            </div>
        </div>
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
.menu {
    position:fixed;
    background: #fffff0;
    top: 0;
    left: 0;
    width: 100%;
    border-bottom: 1px solid #A8A8A8;
    height: 3.5rem;
    overflow: hidden;
}
.menu a.home {
    float: left;
    display: block;
    color: #00A000;
    text-align: center;
    text-decoration: none;
    padding: 5px 35px;
    font-size: 30px;
    font-family: 'Permanent Marker', cursive;

}
.menu .search-container,
.menu a.sign{
    float: right;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #A0A0A0;
    text-decoration: none;
    padding: 8px 35px;
    font-size: 17px;
}
.menu button:hover,
.menu button:active{
  color: #00A000;
}
.menu .input{
    font-size: 25px;
    border: none;
    outline:#00A000;
}
.menu .search-container .search {
    background: #fffff0;
    color: #A0A0A0;
    font-size: 17px;
    border: none;
    cursor: pointer;
    outline: none;
}
.menu .search-container .search:active,
.menu .search-container .search:hover{
    color: #00A000;
}
.menu button{
    background: #fff;
    color: #A0A0A0;
    font-size: 17px;
    border: 1px solid #A0A0A0;
    border-radius: 3px;
    cursor: pointer;
    outline: none;
}
@media screen and (max-width: 600px) {
    .menu .search-container {
        float: none;
    }
    .menu a, .menu input[type=text], .menu .search-container button {
        float: none;
        display: block;
        text-align: left;
        width: 100%;
        margin: 0;
        padding: 14px;
    }
    .menu input[type=text] {
        border: 1px solid #ccc;  
    }
}
</style>
