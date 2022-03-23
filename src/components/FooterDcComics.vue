<template>
  <footer>
      <div class="main-footer">
        <div class="col-left">
          <div class="col-4">
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
          </div>
          <div class="col-4">
            <ul class="dc">
            <li class="title-li">dc</li>
            <li v-for="link in linksDc" :key="link.text">
              <a :href="link.href">{{ link.text }}</a>
            </li>
          </ul>
          </div>
          <div class="col-4">
            <ul class="sites">
            <li class="title-li">sites</li>
            <li v-for="link in linksSites" :key="link.text">
              <a :href="link.href">{{ link.text }}</a>
            </li>
          </ul>
          </div>
        </div>
        <div class="col-right">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
      <div class="footer-social">
        <div class="col-left">
          <button>sign-up now!</button>
        </div>
        <div class="col-right">
          <ul class="social-logos">
            <li><a href="#!">follow us</a></li>
            <li><a href="#!"><img src="../assets/img/footer-twitter.png" alt=""></a></li>
            <li><a href="#!"><img src="../assets/img/footer-twitter.png" alt=""></a></li>
            <li><a href="#!"><img src="../assets/img/footer-youtube.png" alt=""></a></li>
            <li><a href="#!"><img src="../assets/img/footer-pinterest.png" alt=""></a></li>
            <li><a href="#!"><img src="../assets/img/footer-periscope.png" alt=""></a></li>
          </ul>
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
@import "../assets/styles/partials/variables";
footer {
  height: 400px;
  background-image: url(../assets/img/footer-bg.jpg);
}
.main-footer {
  display: flex;
  .col-left {
  width: 50%;
  height: 400px;
  display: contents;
  flex-direction: column;
  flex-wrap: wrap;
  color: white;
  margin-top: 30px;
  ul {
    li {
      list-style: none;
      margin: 3px 0;
      a {
        color: gray;
        text-decoration: none;
      }
    }
    .title-li {
      font-weight: 700;
      color: white;
      text-transform: uppercase;
      font-size: 1.5rem;
    }
  }
}
}

.col-4 {
  width: 15%;
  margin: 30px;
  font-size: 1.2rem;
}
.col-right {
  width: 50%;
  height: 400px;
  /* position: relative; */
  overflow: hidden;
 /*  img {
    position: absolute;
    top: -23%;
  } */
}
.footer-social {
  background-color: rgb(19%, 19%, 19%);
  display: flex;
  height: 100px;
  align-items: center;
  justify-content: space-between;
  .col-right {
    height: 100%;
    display: flex;
    align-items: center;
  justify-content: center;
  }
  img {
    width: 35px;
  }
  button {
    height: 50px;
    background: transparent;
    border: 3px solid $blue_logo_color;
    color: white;
    text-transform: uppercase;
    padding: 15px;
    font-weight: 700;
    margin-left: 100px;
  }
  ul {
    display: flex;
    justify-content: space-between;
    flex-grow: .3;
    align-items: center;
    list-style: none;
    color: $blue_logo_color;
    text-transform: uppercase;
    font-weight: 600;
    font-size: 1.2rem;
    a{
      text-decoration: none;
      color: $blue_logo_color
    }
  }
}
</style>
