<template>
    <article class="container">
        <div 
        class="post-preview-thumbnail"
        :style="{ backgroundImage: 'url('+ thumbnailUrl +')' }">
        </div>
        <div class="post-preview-title">
            <h1>{{ title }}</h1>
        </div>
        <div class="post-preview-content">
            <p>{{ resume }}</p>
        </div> 
        <div class="linked">
            <nuxt-link to="stars/">
                <a>continuer à lire....</a>
            </nuxt-link>
        </div>
    </article>
</template>

<script>

export default {
    
    props:{
        title:{
            type: String,
            required: true
        },
        resume:{
            type: String,
            required: true
        },
        thumbnailUrl:{
            type: String,
            required: true
        },
        id:{
            type: String,
            required: true
        }
    }
}
</script>

<style scoped>

.container{
    position: relative;
    text-align: center;
    color: white;
    border-radius: 3px;
    box-shadow: 1px 1px 5px 1px rgba(0, 0, 0, 0.5);
    background:  rgba(0, 0, 0, 0.8);
    width: 90%;
    margin: 4rem;
    height: 20rem;  
}
.post-preview-thumbnail{
    float: right;
    background-size: cover;
    background-position:right;
    height: 20rem;
    width: 50%;
    border-radius: 3px;
    margin-right: -15px;
}
.post-preview-title{
    padding-top: 40px;
    text-align: center;
    font-style: italic;
}
.post-preview-content,
.linked{
    padding-top: 20px;
    text-align: center;
    font-size: large;
    font-style: italic;
}
a p{
    text-decoration: none;
    color: white;
    font-weight: bolder;
}
@media (min-width: 35rem){
    .post-preview{
        width: 25rem;
    }
} 

/*.post-preview {
    border-radius: 3px;
    box-shadow: 1px 1px 5px 1px rgba(0, 0, 0, 0.5);
    width: 90%;
    margin: 1rem;
    height: 20rem;
}

.post-preview-thumbnail{
    background-position: center;
    background-size: cover;
    width: 80%;
    height: 10rem;
}

.post-preview-content{
    text-align: center;
    padding: 1rem;
}

@media (min-width: 35rem){
    .post-preview{
        width: 25rem;
    }
} */
</style>


