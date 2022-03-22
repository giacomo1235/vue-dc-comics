<template>
  <footer>
      <div class="main-footer">
        <div class="col-left">
          <ul id="dcComics">
            <li class="title-li">dc comics</li>
            <li v-for="link in linksComics" :key="link.text">
              <a :href="link.href">{{ link.text }}</a>
            </li>
          </ul>
          <ul id="shop">
            <li class="title-li">shop</li>
            <li v-for="link in linksShop" :key="link.text">
              <a :href="link.href">{{ link.text }}</a>
            </li>
          </ul>
          <ul class="dc">
            <li class="title-li">dc</li>
            <li v-for="link in linksDc" :key="link.text">
              <a :href="link.href">{{ link.text }}</a>
            </li>
          </ul>
          <ul class="sites">
            <li class="title-li">sites</li>
            <li v-for="link in linksSites" :key="link.text">
              <a :href="link.href">{{ link.text }}</a>
            </li>
          </ul>
        </div>
        <div class="col-right">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterDcComics',
  data () {
    return {
      linksComics: [
        {
          href: '#!',
          text: 'Characters'
        },
        {
          href: '#!',
          text: 'Comics'
        },
        {
          href: '#!',
          text: 'Movies'
        },
        {
          href: '#!',
          text: 'Tv'
        },
        {
          href: '#!',
          text: 'Games'
        },
        {
          href: '#!',
          text: 'Colectibles'
        },
        {
          href: '#!',
          text: 'Videos'
        },
        {
          href: '#!',
          text: 'News'
        }
      ],
      linksShop: [
        {
          href: '#!',
          text: 'Shop DC'
        },
        {
          href: '#!',
          text: 'Shop DC collectibles'
        }
      ],
      linksDc: [
        {
          href: '#!',
          text: 'Terms Of Use'
        },
        {
          href: '#!',
          text: 'Privacy policy (New)'
        },
        {
          href: '#!',
          text: 'Ad Choices'
        },
        {
          href: '#!',
          text: 'Advertising'
        },
        {
          href: '#!',
          text: 'Jobs'
        },
        {
          href: '#!',
          text: 'Subscriptions'
        },
        {
          href: '#!',
          text: 'Talent Workshops'
        },
        {
          href: '#!',
          text: 'CPSC Certificates'
        },
        {
          href: '#!',
          text: 'Ratings'
        },
        {
          href: '#!',
          text: 'Shop Help'
        },
        {
          href: '#!',
          text: 'Contact Us'
        }
      ],
      linksSites: [
        {
          href: '#!',
          text: 'DC'
        },
        {
          href: '#!',
          text: 'MAD Magazine'
        },
        {
          href: '#!',
          text: 'DC Kids'
        },
        {
          href: '#!',
          text: 'DC Universe'
        },
        {
          href: '#!',
          text: 'DC Power Visa'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import "@/assets/styles/partials/variables";
footer {
  height: 400px;
  background-image: url(../assets/img/footer-bg.jpg);
}
.main-footer {
  display: flex;
}

.col-left {
  width: 50%;
  height: 400px;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  color: white;
  ul {
    li {
      list-style: none;
      a {
        color: gray;
        text-decoration: none;
      }
    }
    .title-li {
      font-weight: 700;
      color: white;
      text-transform: uppercase;
    }
  }
}
.col-right {
  width: 50%;
  height: 400px;
  position: relative;
  overflow: hidden;
  img {
    position: absolute;
    top: -10%;
  }
}
</style>
