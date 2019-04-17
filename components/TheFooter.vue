<template>

<div class="footer">
    <nuxt-link><a><font-awesome-icon icon="fa-twitter" /></a></nuxt-link>
</div>

    
</template>

<script>

import { library } from '@fortawesome/fontawesome-svg-core'
import { faTwitter } from '@fortawesome/free-solid-svg-icons'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
library.add(faTwitter)

export default {
    
}
</script>

<style>
.footer {
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    height: 5rem;
    background-color: #fffff0;
    color: #A8A8A8;
    text-align: center;
}

</style>


