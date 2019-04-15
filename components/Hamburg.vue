<template>
    <article>
      <Posted
        v-for="post in posts"
        :key="post.id"
        :title="post.title"
        :excerpt="post.excerpt"
        :thumbnailImage="post.thumbnailImage"
        :id="post.id"/>
    </article>
</template>

<script>
import Posted from '~/components/Posted.vue'

export default {

    components:{
        Posted
    },

    asyncData(context){
        return context.app.$storyapi.get('cdn/stories', {
            version: 'draft' ,  starts_with: 'preview/'
        }).then( res => {
            return {
                posts: res.data.stories.map( bp => {
                    return{
                        title: bp.content.title,
                        excerpt: bp.content.summary,
                        thumbnailImage: bp.content.thumbnail,
                        id: bp.slug
                    }
                })
            }
        })
    } 
}
</script>

