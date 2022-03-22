<template>
  <footer>
    <div class="container">
      <nav>
        <div>
          <h2>dc comics</h2>
          <a v-for="(link, index) in dcComics" :key="index" :href="link.href">{{ link.text }}</a>
        </div>
        <div>
          <h2>shop</h2>
          <a v-for="(link, index) in shop" :key="index" :href="link.href">{{ link.text }}</a>
        </div>
        <div>
          <h2>dc</h2>
          <a v-for="(link, index) in dc" :key="index" :href="link.href">{{ link.text }}</a>
        </div>
        <div>
          <h2>sites</h2>
          <a v-for="(link, index) in sites" :key="index" :href="link.href">{{ link.text }}</a>
        </div>
      </nav>
    </div>
    <SocialBar />
  </footer>
</template>

<script>
import SocialBar from './SocialBar.vue'

export default {
  name: 'FooterSite',
  data () {
    return {
      dcComics: [
        {
          href: '#',
          text: 'characters'
        },
        {
          href: '#',
          text: 'comics'
        },
        {
          href: '#',
          text: 'movies'
        },
        {
          href: '#',
          text: 'TV'
        },
        {
          href: '#',
          text: 'games'
        },
        {
          href: '#',
          text: 'videos'
        },
        {
          href: '#',
          text: 'news'
        }
      ],
      shop: [
        {
          href: '#',
          text: 'shop DC'
        },
        {
          href: '#',
          text: 'shop DC collectibles'
        }
      ],
      dc: [
        {
          href: '#',
          text: 'terms of use'
        },
        {
          href: '#',
          text: 'privacy'
        },
        {
          href: '#',
          text: 'ad choice'
        },
        {
          href: '#',
          text: 'advertising'
        },
        {
          href: '#',
          text: 'jobs'
        },
        {
          href: '#',
          text: 'subscriptions'
        },
        {
          href: '#',
          text: 'talent workshops'
        },
        {
          href: '#',
          text: 'CPSC certificates'
        },
        {
          href: '#',
          text: 'ratings'
        },
        {
          href: '#',
          text: 'shop helps'
        },
        {
          href: '#',
          text: 'contact us'
        }
      ],
      sites: [
        {
          href: '#',
          text: 'DC'
        },
        {
          href: '#',
          text: 'MAD magazines'
        },
        {
          href: '#',
          text: 'DC kids'
        },
        {
          href: '#',
          text: 'DC universe'
        },
        {
          href: '#',
          text: 'DC power visa'
        }
      ],
      socialIcons: [
        {
          alt: 'Facebook',
          img: 'footer-facebook.png',
          link: '#'
        },
        {
          alt: 'Twitter',
          img: 'footer-twitter.png',
          link: '#'
        },
        {
          alt: 'YouTube',
          img: 'footer-youtube.png',
          link: '#'
        },
        {
          alt: 'Pinterest',
          img: 'footer-pinterest.png',
          link: '#'
        },
        {
          alt: 'Periscope',
          img: 'footer-periscope.png',
          link: '#'
        }
      ]
    }
  },
  components: {
    SocialBar
  }
}
</script>

<style scoped lang="scss">
@import '../assets/scss/partials/_variables.scss';

footer {
  background-image: url('../assets/img/footer-bg.jpg');
  padding: 2rem 0 0 0;

    > div {
        display: flex;
        justify-content: space-between;
        background-image: url('../assets/img/dc-logo-bg.png');
        background-position: right center;
        background-repeat: no-repeat;

          img {
            object-fit: cover;
          }
    }
}

nav {
  color: $footer-title-color;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  max-height: 400px;
  align-content: start;

    h2 {
      text-transform: uppercase;
      margin-bottom: 1rem;
    }

    div {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      margin: 1rem 2rem;
      font-size: 0.75rem;
    }
}

a {
  display: block;
  padding: 0.25rem 0;
  color: $footer-menu-color;
  text-transform: capitalize;

    &:hover {
      color: #fff;
    }
}
</style>
