<template>
      <nav>
          <ul>
                <li 
                    v-for="value in navLinks" 
                    v-bind:key="value.id" 
                >
                    <router-link to="{{location}}">{{name}}</router-link>
                </li>
          </ul>
      </nav>
</template>

<script>

export default {
    name: 'Navigation', 
    props: {
        id: Number,
        name: String,
        location: String
    }
}
</script>

<style lang="scss" scoped>
  nav{
      position: fixed;

      ul{
          margin: 0;
          padding: 0;
          list-style: none;
          text-align: right;

          li{
              line-height: 100px;
              display: inline-block;
              padding: 0 1rem;
          }
      }
  }
</style>
