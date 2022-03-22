<template>
  <header>
    <div class="container">
      <img src="@/assets/img/dc-logo.png" alt="logo" />
      <ul>
        <li v-for="link in links" :key="link.text">
          <a :href="link.href">{{ link.text }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
/* eslint-disable */
export default {
  name: 'HeaderDcComics',
  data () {
    return {
      links: [
        {
          href: '#!',
          text: 'characters'
        },
        {
          href: '#!',
          text: 'comics'
        },
        {
          href: '#!',
          text: 'movies'
        },
        {
          href: '#!',
          text: 'tv'
        },
        {
          href: '#!',
          text: 'games'
        },
        {
          href: '#!',
          text: 'colectibles'
        },
        {
          href: '#!',
          text: 'videos'
        },
        {
          href: '#!',
          text: 'fans'
        },
        {
          href: '#!',
          text: 'news'
        },
        {
          href: '#!',
          text: 'shop'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import "@/assets/styles/partials/variables";
.container {
    display: flex;
    justify-content: space-around;
    align-content: center;
}

ul {
  display: flex;
  align-content: center;
  justify-content: space-evenly;
}

li {
    display: flex;
    align-content: center;
    text-align: center;
    padding: 2px 5px;
    a {
        display: inline-block;
        text-decoration: none;
    }
}
</style>
