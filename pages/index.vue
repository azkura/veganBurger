<template>
  <section>
  <!--    <PostPreview />  
      <Hamburg />  -->
      <article id="posts">
      <Posted
        v-for="post in posts"
        :key="post.id"
        :title="post.title"
        :excerpt="post.excerpt"
        :thumbnailImage="post.thumbnailImage"
        :id="post.id"/>
    </article>
  </section>
</template>

<script>

import PostPreview from '~/components/PostPreview.vue'
import Posted from '~/components/Posted.vue'

export default {

  components:{
    PostPreview,
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

<style>

#posts{
  padding-top: 3rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
}
@media (min-width: 35rem){
  #post{
    flex-direction: row;
  }
}

</style>


