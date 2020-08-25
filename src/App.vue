<template>
  <div id="app">
    <Navigation v-bind:navData="navLinks"></Navigation>
    <Header />
    <Content 
      title="Hi I am Ben Coenjaerts &#128400;" 
      subTitle="Wordpress Developer and Graphic Designer from Luxembourg"
    >
    </Content>
    <div class="container-fluid py-5">
      <div class="container grid">
        <Work 
          v-for="value in workValue" 
          v-bind:key="value.id" 
          
          :name="value.name" 
          :image="value.image"
          :url="value.url"
        />
      </div>
    </div>

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import Work from './components/Work.vue'
import Navigation from './components/Navigation.vue'

export default {
  name: 'App',
  components: {
    Header,
    Content,
    Work,
    Navigation
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

<style lang="scss">
  /* MAIN */

  *{
    box-sizing: border-box;
  }
  body{
    padding: 0;
    margin: 0;
    overflow-x: hidden;
    font-family: $font1;
    font-size: 1.2em;
    background-color: $white;
  }
  .container-fluid{
    width: 100vw;
  }
  .container{
    width: 100%;
    max-width: 1200px;
    margin: auto;
  }

  /* FORMATTING */
  h1{
    margin: 0;
    padding: 0;
    font-size: 1.5em;
    color: $grey;
  }
  h2{
    margin: 0;
    padding: 0;
    font-size: 1.8em;
    color: $black;
  }
  a{
    text-decoration: none;
    color: $grey;
    transition: 0.5s;

    &:hover{
      color: $black;
    }
  }
</style>
