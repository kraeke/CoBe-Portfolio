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
    width: 48%;
    display: inline-block;
    margin-bottom: 2%;
    transition: 0.5s;

    &:hover{
      transform: scale(1.1);

      .work-name{
        &::before{
          background-color: $color2;
        }
      }
    }
    &:first-child{
      margin-left: 0;
      margin-right: 2%;
    }
    &:nth-child(2n){
      margin-left: 2%;
      margin-right: 0;
    }
    &:nth-child(3n){
      width: 100%;
      margin: 0 0 2% !important;
    }
    &:nth-child(4n){
      width: 34%;
      margin-left: 0;
      margin-right: 2%;
    }
    &:nth-child(5n){
      width: 62%;
      margin-left: 2%;
      margin-right: 0;
    }
    
    .work-image{
      width: 100%;
      height: 400px;
      background-size: cover;
      background-position: center;
    }
    .work-name{
      display: inline-block;
      line-height: 3em;

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
