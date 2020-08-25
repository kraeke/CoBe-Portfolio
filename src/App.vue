<template>
  <div id="app">
    <nav :style="{fontSize : isLight}">
      <div><router-link to="/">Home</router-link></div>
      <div><router-link to="/Work">Work</router-link></div>
      <div><router-link to="/About">About</router-link></div>
    </nav>
    <router-view/>
  </div>
</template>

<script>
  export default {
    data: function() {
      return {
        isLight: 1
      };
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

  /* NAVIGATION */

  nav{
    position: fixed;
    line-height: 100px;
    padding: 0 1rem;

    div{
      display: inline-block;
      padding: 0 1rem;

      a{
        color: white;
      }
    }
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
