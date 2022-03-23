<template>
<main>
    <div class="container">
        <div class="contents">
          <CardHero v-for="hero in arrHeroes" :key="hero.series" :card-thumb="hero.thumb" :card-serie="hero.series" />
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
import CardHero from '../components/CardHero.vue'
/* import json from '../../public/dc-comics.json' */
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
      ],
      arrHeroes: [
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX',
          price: '$19.99',
          series: 'Action Comics',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01',
          price: '$3.99',
          series: 'American Vampire 1976',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb',
          price: '$16.99',
          series: 'Aquaman',
          type: 'graphic novel'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76',
          price: '$2.99',
          series: 'Batgirl',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          price: '$3.99',
          series: 'Batman',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ',
          price: '$2.99',
          series: 'Batman Beyond',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8',
          price: '$3.99',
          series: 'Batman/Superman',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk',
          price: '$4.99',
          series: 'Batman/Superman Annual',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8',
          price: '$5.99',
          series: 'Batman: The Joker War Zone',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY',
          price: '$6.99',
          series: 'Batman: Three Jokers',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX',
          price: '$4.99',
          series: 'Batman: White Knight Presents: Harley Quinn',
          type: 'comic book'
        },
        {
          thumb: 'https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq',
          price: '$16.99',
          series: 'Catwoman',
          type: 'graphic novel'
        }
      ]
    }
  },
  components: {
    CardHero
  }

}

</script>

<style scoped lang="scss">
@import "../assets/styles/partials/variables";
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
