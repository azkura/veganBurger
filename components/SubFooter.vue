<template>
<footer class="footer">
    <nav class="container">
        <div class="about-us">
            <nuxt-link class="home-logo" to=""><a>veg | Ham </a></nuxt-link>
            <p class="devise">another way to eat burgers!
                <br>eat fast but healthy
            </p>
        </div>
        <div class="social-media-link">
            <div class="medias">
                <ul class="social-media-list">
                    <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'twitter']"/></a></nuxt-link>
                    <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'facebook']"/></a></nuxt-link>
                    <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fas', 'camera-retro']"/></a></nuxt-link>
                    <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'youtube-square']"/></a></nuxt-link>
                </ul>
            </div>
            <div>
                <ul class="sponsors">
                    <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'tripadvisor']"/></a></nuxt-link>
                    <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'airbnb']"/></a></nuxt-link>
                    <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'stripe']"/></a></nuxt-link>
                    <nuxt-link class="media-link" to="" tag="li"><a class="icon"><font-awesome-icon :icon="['fab', 'linkedin']"/></a></nuxt-link>
                </ul>
            </div>    
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

<style scoped>
.footer {
    left: 0;
    bottom: 0;
    width: 100%;
    background-color: #fffff0;
}
.container{
    height: 100%;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    grid-auto-rows: 150px;
}
.home-logo {
    font-family: 'Permanent Marker', cursive;
    color: #00A000;
}
.devise,
.contact-link {
    font-family: 'Permanent Marker', cursive;
    color: #A8A8A8;
}
.social-media-link{
    height: 100%;
}
.social-media-list,
.sponsors{
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.media-link,
.contact-link{
    list-style: none;
}
.icon{
    display: block;
    padding: 20px;
    font-size: 25px;
    width: 25px;
    border-radius: 50%;
    color: #00A000;   
}
.contact{
    height: 100%;
}
.contact-links{
    display: flex;
    flex-flow: column wrap;
    align-items: flex-end;
    justify-content: center;
}
 .contact-link .link{
    text-decoration: none;
    color: #A8A8A8;
}
.contact-link .link:active,
.contact-link .link:hover{
    color: #00A000;
}

</style>


