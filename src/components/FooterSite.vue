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
@import '../assets/scss/partials/_mixin.scss';

footer {
  background-image: url('../assets/img/footer-bg.jpg');

  > div {
      @include flex(row, space-between);
      padding: 2rem 0.5rem;
      background-image: url('../assets/img/dc-logo-bg.png');
      background-position: right center;
      background-repeat: no-repeat;

      img {
        object-fit: cover;
      }
  }
}

nav {
  @include flex(column, start, start, wrap);
  color: $footer-title-color;
  max-height: 400px;

  h2 {
    text-transform: uppercase;
    margin-bottom: 1rem;
  }

  div {
    @include flex(column, start, start, wrap);
    margin: 0 2rem 1rem 0;
    font-size: 0.75rem;
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
}

</style>
