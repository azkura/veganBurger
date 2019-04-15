<template>
    <article  class="post-preview">
        <div class="post-preview-content">
            <h1>{{ title }}</h1>
            <p>{{ excerpt }}</p>
        </div>
        <div 
        class="post-preview-thumbnail"
        :style="{ backgroundImage: 'url('+ thumbnailImage +')' }">
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
    }
}
</script>

<style scoped>
.post-preview {

    position: relative;
    text-align: center;
    border-radius: 3px;
    border: 1px solid #A9A9A9;
    box-shadow: 1px 1px 5px 1px rgba(0, 0, 0, 0.3);
    width: 90%; 
    margin: 4rem;
    height: 15rem;  
    display: flex; 
    flex-direction:row;
}
.post-preview-thumbnail{
    background-size: cover;
    background-position:center;
    width: 50%;
}
.post-preview-content{
    text-align: center;
    padding: 1rem;
}
@media (min-width: 35rem){
    .post-preview{
        width: 35rem;
    }
} 
</style>


