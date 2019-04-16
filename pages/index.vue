<template>
  <section class="container">
      <article id="feat">
        <Featured 
          :id="id"
          :title="title"
          :resume="resume"
          :thumbnail="thumbnail"/>
      </article>
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

import Featured from '~/components/Featured.vue'
import Posted from '~/components/Posted.vue'

export default {

  components:{
    Featured,
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
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: row;
}
#feat{
  margin-top: -50px;
 /* margin-bottom: -60px; */
}
@media (min-width: 35rem){
  #post{
    flex-direction: row;
  }
}
</style>


