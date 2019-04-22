<template>

<div class="grid-container">
  <div class="item1">
    <subMenu />
  </div>
  <div class="item2">
    <Featured 
        :id="id"
        :title="title"
        :resume="resume"
        :thumbnail="thumbnail"/>
  </div>
  <div class="item3">
      <Posted 
        v-for="post in posts"
        :key="post.id"
        :title="post.title"
        :excerpt="post.excerpt"
        :thumbnailImage="post.thumbnailImage"
        :id="post.id"/>
  </div>  
  <div class="item4">main</div>
  <div class="item5">Footer</div>
</div>

</template>

<script>

import subMenu from '~/components/subMenu.vue'
import Posted from '~/components/Posted.vue'
import Featured from '~/components/Featured.vue'

export default {
    components:{
    Posted,
    Featured,
    subMenu
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
.grid-container {
  height: 100%;
  display: grid;
  grid-template-areas:
    'header header header header header header'
    'menu menu menu menu menu menu'
    '. . main main . .'
    'footer footer footer footer footer footer';

  grid-gap: 10px;
  background-color: #2196F3;
  padding: 10px;
}

.item1 { grid-area: header; }

.item2 { 
  grid-area: menu; 
}
.item3 { 
  grid-area: main; 

  display:flex;
  flex-direction: row;
  justify-content: space-between;
}

.item4 { grid-area: right; }
.item5 { grid-area: footer; }

</style>



























  

