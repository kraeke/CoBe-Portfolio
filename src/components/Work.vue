<template>
      <a href="" class="work">
        <div class="work-image" :style="{ backgroundImage: 'url(' + image + ')' }"></div>
        <div class="work-name">{{name}}</div> 
      </a>
</template>

<script>

export default {
    name: 'Work',
    props: {
        id: Number,
        name: String,
        image: String,
        url: String
    }
}
</script>

<style lang="scss" scoped>
  .work{
    transition: 0.5s;
    grid-column: span 2;

    &:hover{
      .work-name{
        &::before{
          background-color: $color2;
        }
      }
    }
    &:first-child{
      grid-column: span 3 ;
    }
    &:nth-child(2n){
      grid-column: span 2;
      grid-row: span 2;
    }
    &:nth-child(3n){ 
      grid-column: span 3;
    }
    &:nth-child(4n){
      grid-column: span 2;
    }
    &:nth-child(5n){
      grid-column: span 3;
    }
    &:nth-child(10){
      grid-column: span 3;
      grid-row: span 1;
    }
    
    .work-image{
      width: 100%;
      height: calc(100% - 3rem);
      background-size: cover;
      background-position: center;
    }
    .work-name{
      display: inline-block;
      line-height: 3rem;

      &::before{
        content: "";
        width: 10px;
        height: 10px;
        background-color: $color1;
        display: inline-block;
        border-radius: 5px;
        margin: 0 0.5em 2px 0;
        padding: 0;
        transition: 0.5s;
      }
    }
  }
</style>
