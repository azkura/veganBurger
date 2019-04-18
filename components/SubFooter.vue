<template>
<footer class="main-footer">
    <nav class="footer-nav">
        <div class=".social-media">
            <nuxt-link class="home-logo" to=""><a>veg | Ham </a></nuxt-link>
            <p class="devise">another way to eat burgers!
                <br>eat fast but healthy
            </p>
            <ul class="social-media-list">
                <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'twitter']"/></a></nuxt-link>
                <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'facebook']"/></a></nuxt-link>
                <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'instagram']"/></a></nuxt-link>
                <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'youtube']"/></a></nuxt-link>
            </ul>
        </div>
        <div class="contact">
            <ul class="contact-links">
                <nuxt-link class="contact-link" to="" tag="li"><a class="link">about</a></nuxt-link>
                <nuxt-link class="contact-link" to="" tag="li"><a class="link">all posts</a></nuxt-link>
                <nuxt-link class="contact-link" to="" tag="li"><a class="link">contact us</a></nuxt-link>
                <nuxt-link class="contact-link" to="" tag="li"><a class="link">faq</a></nuxt-link>
            </ul>
        </div>
    </nav>
</footer>
</template>

<script>


export default {
    
}
</script>

<style scoped>
.main-footer {
    width: 100%;
    background-color: #fffff0;
    color: #A8A8A8;
}
.footer-nav{
    height: 100%;
}
.social-media,
.social-media-list {
    float: left;
}
.social-media-list{
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
}
.media-link{
    padding: 0.2rem;
}
.icon{
    display: block;
    background-color: #fffff0;
    padding: 20px;
    font-size: 25px;
    width: 25px;
    border-radius: 50%;
    color: #00A000;   
}
.home-logo {
    font-family: 'Permanent Marker', cursive;
    color: #00A000;
    padding: 10px 1em 0 2em;
}
.devise {
    margin-top: 0;
    margin-bottom: 0rem;
    font-family: 'Permanent Marker', cursive;
    padding: 10px 1em 0 2em;
}
.contact{
    
}
.contact-links{
    display: block;
    margin-left: 450px;
    height: 100%;
    padding: 1px;
}
.contact-link{
    list-style: none;
}
.contact-link .link{
    color: #A8A8A8;
    font-family: 'Permanent Marker', cursive;
    text-decoration: none;
}
.contact-link .link:active,
.contact-link .link:hover{
    color: #00A000;
}
</style>


