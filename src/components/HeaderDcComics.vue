<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="logo" />
      <ul>
        <li v-for="link in links" :key="link.text">
          <a :href="link.href">{{ link.text }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
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
@import "../assets/styles/partials/variables";
.container {
  width: 100%;
    display: flex;
    justify-content: space-around;
    align-content: center;
    /* padding: 20px; */
}
img {
  padding: 5px;
}

ul {
  display: flex;
  align-content: center;
  justify-content: space-evenly;
}

li {
    text-transform: uppercase;
    display: flex;
    padding: 20px;
    padding-bottom: 0;
    a {
        padding: 20px 0;
        color: black;
        font-weight:600;
        display: inline-block;
        text-decoration: none;
        border-bottom: 5px solid transparent;
        &:hover {
          color: $blue_logo_color;
          border-bottom: 5px solid $blue_logo_color;
        }
    }
}
</style>
