<template>
    <div  class="post-preview">
        <div class="post-preview-content">
            <h1>{{ title }}</h1>
            <span>{{datePost}}</span>
            <p>{{ excerpt }}</p>
            <nuxt-link to="">
                <a>continuer la lecture...</a>
            </nuxt-link>
        </div>
        <div 
        class="post-preview-thumbnail"
        :style="{ backgroundImage: 'url('+ thumbnailImage +')' }">
        </div>
    </div>
</template>

<script>
import moment from 'moment'
moment.locale('fr')

export default {
    
    props:{
        title:{
            type: String,
            required: true
        },
        excerpt:{
            type: String,
            required: true
        },
        thumbnailImage:{
            type: String,
            required: true
        },
        id:{
            type:String,
            required:true
        }
    },

    data(){
        return {
            datePost: moment().format('MMM Do')
        }
    }
}
</script>

<style scoped>
.post-preview {
    position: relative;
    border-radius: 4px;
    border: 1px #696969;
    box-shadow: 1px 1px 5px 1px rgba(169, 169, 169, 0.2);
    background: #fffff0;
   /* width: 90%; 
    margin: 1rem;  
    height: 15rem;  */
}
.post-preview-thumbnail{
    background-size: cover;
    background-position:center;
    width: 50%;
    border-radius: 4px;
}
.post-preview-content{
    text-align:left;
    padding: 1rem; 
    color: #A0A0A0;
   /* margin: 3rem; */
}
.post-preview-content h1{
    font-family: 'Permanent Marker', cursive;
}
a{
    text-decoration: none;
    color: #A0A0A0;
}
span{
   font-size: smaller;
    color: #A9A9A9;
}
@media (min-width: 35rem){
    .post-preview{
        width: 35rem;
    }
} 
</style>


