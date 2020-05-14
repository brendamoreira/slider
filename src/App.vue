<template>
  <div id="app">
    <list-images :photos="photos" @select="selectIndex"/>
    <slider :photos="photos" :index="index"/>
  </div>
</template>

<script>
import ListImages from './components/ListImages.vue'
import Slider from './components/Slider.vue'

export default {
  data () {
    return {
      photos: ['https://images.unsplash.com/photo-1589009602500-c5137f420e80?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=600&ixlib=rb-1.2.1&q=80&w=800', 'https://images.unsplash.com/photo-1587725544257-9ae9f910ae8a?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=600&ixlib=rb-1.2.1&q=80&w=800', 'https://images.unsplash.com/photo-1586953805370-9300364ab6f7?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=600&ixlib=rb-1.2.1&q=80&w=800'],
      index: 0
    }
  },
  components: {
    ListImages, 
    Slider
  },
  methods: {
    selectIndex(index){
      this.index = index
    },
    changeIndex(){
      if(this.index + 1 >= this.photos.length){
          this.index = 0
      } else{
        this.index += 1
      }
    }
  },
  created() {
    setInterval(this.changeIndex, 2000)
  }
}
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
  display: flex;
}
</style>
