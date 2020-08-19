<template>
  <header>
    <img src="@/assets/images/logo.svg" alt="CoBe">
  </header>
</template>

<script>
export default {
  name: 'Header',
  props: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
  header{
    width: 100vw;
    height: 100vh;
    background: $color1;
    background: -webkit-linear-gradient(60deg, $color1, $color2);
    background: linear-gradient(60deg, $color1, $color2);
    text-align: center;
    color: white;

    img{
      width: 15%;
      margin-top: 30%;
      transition: 0.5s;
      animation-name: rotate-logo;
      animation-duration: 2s;
      animation-delay: 0.5s;

      &:hover{
        transform: scale(0.95);
        animation-name: rotate-logo;
        animation-duration: 2s;
        animation-delay: 1s;
      }
      @keyframes rotate-logo {
        10%{
            transform: rotate(15deg);
        }
        20%{
            transform: rotate(5deg);
        }
        30%{
            transform: rotate(15deg);
        }
        40%{
            transform: rotate(5deg);
        }
        50%{
            transform: rotate(0deg);
        }
      }
    }
    h2{
      font-weight: normal;
    }
  }
</style>
