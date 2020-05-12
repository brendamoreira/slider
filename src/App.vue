<template>
  <div id="app">
    <list-images :photos="photos"/>
    <img :src="photos[0]" />
  </div>
</template>

<script>
import ListImages from './components/ListImages.vue'

export default {
  data () {
    return {
      photos: ['https://images.unsplash.com/photo-1589009602500-c5137f420e80?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=600&ixlib=rb-1.2.1&q=80&w=800', 'https://images.unsplash.com/photo-1587725544257-9ae9f910ae8a?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=600&ixlib=rb-1.2.1&q=80&w=800', 'https://images.unsplash.com/photo-1586953805370-9300364ab6f7?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=600&ixlib=rb-1.2.1&q=80&w=800']
    }
  },
  components: {
    ListImages
  }
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
</style>
