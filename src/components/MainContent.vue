<template>
<main>
    <div class="container">
        <div class="contents">
          <h1>Content goes here</h1>
        </div>
        <ul class="cards">
          <li v-for="card in cards" :key="card.text">
            <img :src="card.image"  :alt="card.text"> <!-- con card.image non va :src="require('../assets/img/' + card.image)" -->
            <a :href="card.href">{{ card.text }}</a>
          </li>
        </ul>
    </div>
</main>
</template>

<script>
export default {
  name: 'MainContent',
  data () {
    return {
      activeIndex: 1,
      cards: [
        {
          href: '#!',
          text: 'digital comics',
          image: 'buy-comics-digital-comics.png'
        },
        {
          href: '#!',
          text: 'dc merchandise',
          image: 'buy-comics-merchandise.png'
        },
        {
          href: '#!',
          text: 'subscription',
          image: 'buy-comics-subscriptions.png'
        },
        {
          href: '#!',
          text: 'comic shop locator',
          image: 'buy-comics-shop-locator.png'
        },
        {
          href: '#!',
          text: 'dc power visa',
          image: 'buy-dc-power-visa.svg'
        }

      ]
    }
  }
}

</script>

<style scoped lang="scss">
@import "@/assets/styles/partials/variables";
.contents {
  background-color: black;
  color: white;
  height: 133px;
  display: flex;
  align-items: center;
  h1 {
    margin-left: 100px;
  }
}
.cards {
  background-color: $blue_logo_color;
  display: flex;
  justify-content: center;
  list-style: none;
  height: 133px;
  img {
    width: 70px;
    padding: 10px;
  }
  li {
    display: flex;
    align-items: center;
    justify-content: center;
    text-transform: uppercase;
    margin: 30px;
    a {
      text-decoration: none;
      color: white;
      font-size: .9rem;
      font-weight: 500;
    }
  }
}
</style>
