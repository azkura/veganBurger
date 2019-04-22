<template>
<header class="header">
    <nav class="container">
        <div class="menu">
            <nuxt-link to=""><a class="home">VEG | HAM </a></nuxt-link>
        </div>
        <div class="search">
            <form>
                <input type="text" class="input">
            </form>
             <button type="submit" class="icon-search"><font-awesome-icon :icon="['fas', 'search']"/></button>
        </div>
        <div class="sign">
            <nuxt-link to="" class="sign"><button class="connect">sign in</button></nuxt-link>
            <nuxt-link to="" class="sign"><button class="connect">sign out</button></nuxt-link>
            <nuxt-link to="" class="sign"><button class="connect">subscrire</button></nuxt-link>
         </div>
    </nav>
</header>
</template>

<style scoped>

.header{

    height: 100%;
    background: #fffff0;
    top: 0;
    left: 0;
}
.container{
    height: 100%;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(70px, 1fr));
    grid-auto-rows: 50px; 
}
.menu,.search{
    display: flex;
    justify-content: flex-start;
    align-items: center;  
}
.sign{
    display: flex;
    flex-direction: row;
    justify-content:space-between;
    align-items: center;
    text-decoration: none;
}
.connect{
    background: #fff;
    color: #A0A0A0;
    font-size: 17px;
    border: 1px solid #00A000;
    border-radius: 3px;
    cursor: pointer;
    outline: none;
}
.icon-search{
    color: #A0A0A0;
    border: none;
    width: 30px;
    height: 30px;
    border-radius: 3px;
}
.input{
    border: none;
    width: 220px;
    height: 30px;
    border-radius: 3px;
    outline: none;
    border: 1px solid #00A000;
}
.menu a.home{
    color: #00A000;
    font-size: 20px;
    font-family: 'Permanent Marker', cursive;
}
a{
    text-decoration: none; 
}
button:hover,
button:active {
    color: #00A000;
}

</style>
