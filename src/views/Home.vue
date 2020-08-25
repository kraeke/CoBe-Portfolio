<template>
  <div id="app">
    <Header />
    <Content 
      title="Hi I am Ben Coenjaerts &#128400;" 
      subTitle="Wordpress Developer and Graphic Designer from Luxembourg"
    >
    </Content>
    <div class="container grid py-5">
      <Work 
        v-for="value in workValue" 
        v-bind:key="value.id" 
        
        :name="value.name" 
        :image="value.image"
        :url="value.url"
      />
    </div>

  </div>
</template>

<script>
import Header from '../components/Header.vue'
import Content from '../components/Content.vue'
import Work from '../components/Work.vue'

export default {
  name: 'Home',
  components: {
    Header,
    Content,
    Work
  },
  data (){
    return{
      workValue: [
        {id: 0, name: 'Lorem Ipsum', image: 'https://picsum.photos/1920/1080', url: 'project1.html'},
        {id: 1, name: 'Dolor sit amet', image: 'https://picsum.photos/1920/1082', url: 'project1.html'},
        {id: 2, name: 'Sit Ipsum Lorem dolor', image: 'https://picsum.photos/1920/1089', url: 'project1.html'},
        {id: 1, name: 'Dolor sit amet', image: 'https://picsum.photos/1920/1082', url: 'project1.html'},
        {id: 2, name: 'Sit Ipsum Lorem dolor', image: 'https://picsum.photos/1920/1081', url: 'project1.html'},
        {id: 1, name: 'Dolor sit amet', image: 'https://picsum.photos/1920/1042', url: 'project1.html'},
        {id: 2, name: 'Sit Ipsum Lorem dolor', image: 'https://picsum.photos/1920/1051', url: 'project1.html'},
        {id: 2, name: 'Sit Ipsum Lorem dolor', image: 'https://picsum.photos/1920/1082', url: 'project1.html'},
        {id: 2, name: 'Sit Ipsum Lorem dolor', image: 'https://picsum.photos/1920/1181', url: 'project1.html'},
        {id: 2, name: 'Sit Ipsum Lorem dolor', image: 'https://picsum.photos/1920/1281', url: 'project1.html'}
      ],
      navLinks: [
        {id: 0, name: 'Home', location: "/home"},
        {id: 1, name: 'Work', location: "/work"},
        {id: 2, name: 'About me', location: "/about"},
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
  
</style>
