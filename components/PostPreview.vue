<template>
  <section id="vignette">
    <article>
       <Featured
        v-for="feat in feats"
        :key="feat.id"
        :title="feat.title"
        :resume="feat.resume"
        :thumbnailUrl="feat.thumbnailUrl" 
        :id="feat.id"/>
    </article>
  </section>
</template>

<script>
import Featured from '~/components/Featured.vue'

export default {
    
  components: {
    Featured
  },

  asyncData(context){
    return context.app.$storyapi.get('cdn/stories', {
    version: 'draft', starts_with: 'stars/'
    }).then( res => {
      return {
        feats: res.data.stories.map( bf =>{
          return{
            id: bf.slug,
            title: bf.content.title,
            resume: bf.content.summary,
            thumbnailUrl: bf.content.thumbnail
          }
        })
      }
    })
  }
}
</script>
