<template>
  <section id="vignette">
      <Arg
      v-for="feat in feats"
      :key="feat.id"
      :title="feat.title"
      :excerpt="feat.excerpt"
      :thumbnailUrl="feat.thumbnailUrl" 
      :id="feat.id"/>
  </section>
</template>

<script>
import Arg from '~/components/Arg.vue'

export default {
  components: {
    Arg
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
            excerpt: bf.content.summary,
            thumbnailUrl: bf.content.thumbnail
          }
        })
      }
    })
  }
}

</script>

<style>

</style>
