<template>
  <div class="card">
      <img :src="cardThumb" alt="">
      <h2 class="title">{{cardSerie}}</h2>
  </div>
</template>

<script>
export default {
  name: 'CardHero',
  props: {
    cardThumb: String,
    cardSerie: String
  }
}
</script>

<style scoped lang="scss">
.card {
    text-transform: uppercase;
    color: white;
    width: 15%;
    height: 15%;
    overflow: hidden;
    padding: 20px;
    .title{
      font-size: 1rem;
    }
    img {
      width: 192px;
      height: 192px;
    }
}
</style>
