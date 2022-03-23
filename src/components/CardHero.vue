<template>
  <div class="card">
      <img :src="cardThumb" alt="">
      <h2>{{cardSerie}}</h2>
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
}
img {
    width: 150px;
    height: 150px;
}
</style>
