<template>
<footer class="main-footer">
    <div class="copyright">
        <ul class="copy-right">
            <nuxt-link to="/blog" tag="li" class="right">
                <a>{{date}}© all reserved |  made by az</a>
            </nuxt-link>
             <nuxt-link to="" tag="li" class="right">
                <a><font-awesome-icon :icon="['fab', 'github']"/></a>
            </nuxt-link>
        </ul>
    </div>
</footer>
</template>

<script>
import moment from'moment'

export default {

    data(){
        return{
            date: moment().format('YYYY')  
        }
    }
}
</script>


<style scoped>

.main-footer{
    position: fixed;
    left: 0;
    bottom: 0;
    width: 100%;
    background-color: #FCF4A3;
    height: 3rem;
}
.copyright{
    height: 100%;
}
.copy-right{
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
}

.right{
    display:flex;
    justify-content: center;
    align-items: center;
    margin: 0 1rem;
    padding: 0.3rem;
    height: 100%;
}

.right a{
    display: block;
    text-decoration: none;
    color: #A0A0A0;
}
.right a:hover,
.right a:active,
.right.nuxt-link-active a{
    color: #00A000;
}

</style>

