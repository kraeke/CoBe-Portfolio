<template>
  <section class="container-fluid py-5">
    <div class="container">
        <h2 v-if="title">{{title}}</h2>
        <h1 v-if="subTitle">{{subTitle}}</h1>
        <p v-if="paragraph">{{paragraph}}</p>
    </div>
  </section>
</template>

<script>

export default {
  name: 'Content',
  props: {
    title: String,
    subTitle: String,
    paragraph: String,
  }
}
</script>

<style lang="less" scoped>

</style>
